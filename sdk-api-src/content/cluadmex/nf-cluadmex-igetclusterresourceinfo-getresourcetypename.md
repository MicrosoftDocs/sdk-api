---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceTypeName
title: IGetClusterResourceInfo::GetResourceTypeName (cluadmex.h)
description: Returns the type of a resource.
helpviewer_keywords: ["GetResourceTypeName","GetResourceTypeName method [Failover Cluster]","GetResourceTypeName method [Failover Cluster]","IGetClusterResourceInfo interface","IGetClusterResourceInfo interface [Failover Cluster]","GetResourceTypeName method","IGetClusterResourceInfo.GetResourceTypeName","IGetClusterResourceInfo::GetResourceTypeName","_wolf_igetclusterresourceinfo_getresourcetypename","cluadmex/IGetClusterResourceInfo::GetResourceTypeName","mscs.igetclusterresourceinfo_getresourcetypename"]
old-location: mscs\igetclusterresourceinfo_getresourcetypename.htm
tech.root: MsCS
ms.assetid: c7154163-0ab9-4766-99be-31457a0efc17
ms.date: 12/05/2018
ms.keywords: GetResourceTypeName, GetResourceTypeName method [Failover Cluster], GetResourceTypeName method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceTypeName method, IGetClusterResourceInfo.GetResourceTypeName, IGetClusterResourceInfo::GetResourceTypeName, _wolf_igetclusterresourceinfo_getresourcetypename, cluadmex/IGetClusterResourceInfo::GetResourceTypeName, mscs.igetclusterresourceinfo_getresourcetypename
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
 - IGetClusterResourceInfo::GetResourceTypeName
 - cluadmex/IGetClusterResourceInfo::GetResourceTypeName
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
 - IGetClusterResourceInfo.GetResourceTypeName
---

# IGetClusterResourceInfo::GetResourceTypeName


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the type of a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target resource. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

### -param lpszResTypeName [out]

Pointer to the type of the resource associated with <i>lObjIndex</i>. The 
       <i>lpResTypeName</i> parameter can be <b>NULL</b>, indicating that the 
       caller is requesting only the length of the 
       <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>. Although declared as a 
       <b>BSTR</b>, this parameter is implemented as an <b>LPWSTR</b>.

### -param pcchResTypeName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpResTypeName</i> parameter. The <i>pcchResTypeName</i> parameter 
       cannot be <b>NULL</b>. On output, pointer to the count of characters in the resource type 
       name stored in the content of <i>lpResTypeName</i>, including the 
       <b>NULL</b>-terminating character.

## -returns

If <b>GetResourceTypeName</b> 
       is not successful, it can return other <b>HRESULT</b> values.

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
The buffer pointed to by <i>lpResTypeName</i> is too small to hold the requested 
         resource type. 
         <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterresourceinfo-getresourcetypename">GetResourceTypeName</a> 
         returns the required number of characters in the content of <i>pcchResTypeName</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>