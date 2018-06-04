---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# peerdist_status_info_tag structure


## -description


The <b>PEERDIST_STATUS_INFO</b> structure contains information about the current status and capabilities of the BranchCache service on the local computer.


## -struct-fields




### -field cbSize

Size, in bytes, of the <b>PEERDIST_STATUS_INFO</b> structure.


### -field status

Specifies the current status of the BranchCache service. This member should be one of following values defined in the <a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a> enumeration.


### -field dwMinVer

Specifies the  minimum version of the content information format supported by the BranchCache service on the local machine. This member must be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1"></a><a id="peerdist_retrieval_options_contentinfo_version_1"></a><dl>
<dt><b>PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows 7 compatible content information format.

</td>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2"></a><a id="peerdist_retrieval_options_contentinfo_version_2"></a><dl>
<dt><b>PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Windows 8 content information format.

</td>
</tr>
</table>
 


### -field dwMaxVer

 Specifies the  maximum version of the content information format supported by the BranchCache service on the local machine. This member must be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1"></a><a id="peerdist_retrieval_options_contentinfo_version_1"></a><dl>
<dt><b>PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Windows 7 compatible content information format.

</td>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2"></a><a id="peerdist_retrieval_options_contentinfo_version_2"></a><dl>
<dt><b>PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Windows 8 content information format.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a>



<a href="https://msdn.microsoft.com/7D8D3B84-F353-4820-B035-5F289085BE7E">PeerDistGetStatusEx</a>
 

 

