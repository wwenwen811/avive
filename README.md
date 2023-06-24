# avive
avive
int query(int l,int r){
	int ret = 0;
	for (l += treeLen - 1, r += treeLen +1; l ^ r ^ 1; l >>= 1, r >>= 1){
		if (~l & 1)ret = min(ret, val[l^1]);
		if (r & 1)ret = min(ret, val[r ^ 1]);
	}
	return ret;
}
