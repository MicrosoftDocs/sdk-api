---
UID: NF:cluadmex.IGetClusterDataInfo.GetClusterName
title: IGetClusterDataInfo::GetClusterName (cluadmex.h)
description: Returns the name of the cluster. (IGetClusterDataInfo.GetClusterName)
helpviewer_keywords: ["GetClusterName","GetClusterName method [Failover Cluster]","GetClusterName method [Failover Cluster]","IGetClusterDataInfo interface","IGetClusterDataInfo interface [Failover Cluster]","GetClusterName method","IGetClusterDataInfo.GetClusterName","IGetClusterDataInfo::GetClusterName","_wolf_igetclusterdatainfo_getclustername","cluadmex/IGetClusterDataInfo::GetClusterName","mscs.igetclusterdatainfo_getclustername"]
old-location: mscs\igetclusterdatainfo_getclustername.htm
tech.root: MsCS
ms.assetid: 711a193f-de29-4e90-adf1-6dc6e95c0c61
ms.date: 12/05/2018
ms.keywords: GetClusterName, GetClusterName method [Failover Cluster], GetClusterName method [Failover Cluster],IGetClusterDataInfo interface, IGetClusterDataInfo interface [Failover Cluster],GetClusterName method, IGetClusterDataInfo.GetClusterName, IGetClusterDataInfo::GetClusterName, _wolf_igetclusterdatainfo_getclustername, cluadmex/IGetClusterDataInfo::GetClusterName, mscs.igetclusterdatainfo_getclustername
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
 - IGetClusterDataInfo::GetClusterName
 - cluadmex/IGetClusterDataInfo::GetClusterName
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
 - IGetClusterDataInfo.GetClusterName
---

# IGetClusterDataInfo::GetClusterName


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the cluster.

## -parameters

### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the cluster; or 
       <b>NULL</b> to indicate that the caller is requesting only the length of the name. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.

### -param pcchName [in, out]

On input, pointer to the size of the buffer, in characters, pointed to by the 
       <i>lpszName</i> parameter. On output, pointer to the total number of characters in the 
       buffer including the <b>NULL</b>-terminating character.

## -returns

If <b>GetClusterName</b> is not 
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
         <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getclustername">GetClusterName</a> returns the 
         required number of characters in the content of <i>pcchName</i>.

</td>
</tr>
</table>

## -remarks

If the <i>lpszName</i> parameter is set to <b>NULL</b> and the 
     <i>pcchName</i> parameter is not set to <b>NULL</b>, the 
     <b>GetClusterName</b> method returns 
     <b>NOERROR</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>
