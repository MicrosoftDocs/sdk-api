---
UID: NS:peerdist.peerdist_status_info_tag
title: peerdist_status_info_tag
author: windows-sdk-content
description: The PEERDIST_STATUS_INFO structure contains information about the current status and capabilities of the BranchCache service on the local computer.
old-location: p2p\peerdist_status_info.htm
tech.root: P2PSdk
ms.assetid: 6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PPEERDIST_STATUS_INFO, PCPEERDIST_STATUS_INFO, PCPEERDIST_STATUS_INFO structure pointer [Peer Networking], PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1, PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2, PEERDIST_STATUS_INFO, PEERDIST_STATUS_INFO structure [Peer Networking], PPEERDIST_STATUS_INFO, PPEERDIST_STATUS_INFO structure pointer [Peer Networking], p2p.peerdist_status_info, peerdist/PCPEERDIST_STATUS_INFO, peerdist/PEERDIST_STATUS_INFO, peerdist/PPEERDIST_STATUS_INFO, peerdist_status_info_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_STATUS_INFO
product: Windows
targetos: Windows
req.typenames: PEERDIST_STATUS_INFO, *PPEERDIST_STATUS_INFO
req.redist: 
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
 

 

