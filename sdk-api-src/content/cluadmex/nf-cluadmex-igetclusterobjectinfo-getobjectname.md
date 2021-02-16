---
UID: NF:cluadmex.IGetClusterObjectInfo.GetObjectName
title: IGetClusterObjectInfo::GetObjectName (cluadmex.h)
description: Returns the name of a cluster object.
helpviewer_keywords: ["GetObjectName","GetObjectName method [Failover Cluster]","GetObjectName method [Failover Cluster]","IGetClusterObjectInfo interface","IGetClusterObjectInfo interface [Failover Cluster]","GetObjectName method","IGetClusterObjectInfo.GetObjectName","IGetClusterObjectInfo::GetObjectName","_wolf_igetclusterobjectinfo_getobjectname","cluadmex/IGetClusterObjectInfo::GetObjectName","mscs.igetclusterobjectinfo_getobjectname"]
old-location: mscs\igetclusterobjectinfo_getobjectname.htm
tech.root: MsCS
ms.assetid: e45f3652-74da-4d93-826d-320ddae10f49
ms.date: 12/05/2018
ms.keywords: GetObjectName, GetObjectName method [Failover Cluster], GetObjectName method [Failover Cluster],IGetClusterObjectInfo interface, IGetClusterObjectInfo interface [Failover Cluster],GetObjectName method, IGetClusterObjectInfo.GetObjectName, IGetClusterObjectInfo::GetObjectName, _wolf_igetclusterobjectinfo_getobjectname, cluadmex/IGetClusterObjectInfo::GetObjectName, mscs.igetclusterobjectinfo_getobjectname
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetClusterObjectInfo::GetObjectName
 - cluadmex/IGetClusterObjectInfo::GetObjectName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterObjectInfo.GetObjectName
---

# IGetClusterObjectInfo::GetObjectName


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of a <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target object. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the object associated with 
       <i>lObjIndex</i>. The <i>lpszName</i> parameter can be 
       <b>NULL</b>, indicating that the caller is requesting only the name length. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.

### -param pcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszName</i> parameter. The <i>pcchName</i> parameter cannot be 
       <b>NULL</b>. On output, pointer to the count of characters in the name stored in the content 
       of <i>lpszName</i>, including the <b>NULL</b>-terminating character.

## -returns

If <b>GetObjectName</b> is not 
       successful, it can return other <b>HRESULT</b> values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
<dt>0x800700ea</dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpszName</i> is too small to hold the requested name. 
         <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterobjectinfo-getobjectname">GetObjectName</a> returns the 
         required number of characters in the content of <i>pcchName</i>.

</td>
</tr>
</table>

## -remarks

If the <i>lpszName</i> parameter is specified as <b>NULL</b>, the 
     <b>GetObjectName</b> method returns 
     <b>NOERROR</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterobjectinfo">IGetClusterObjectInfo</a>