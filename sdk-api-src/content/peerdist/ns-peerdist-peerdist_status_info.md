---
UID: NS:peerdist.peerdist_status_info_tag
title: PEERDIST_STATUS_INFO (peerdist.h)
description: The PEERDIST_STATUS_INFO structure contains information about the current status and capabilities of the BranchCache service on the local computer.
helpviewer_keywords: ["*PPEERDIST_STATUS_INFO","PCPEERDIST_STATUS_INFO","PCPEERDIST_STATUS_INFO structure pointer [Peer Networking]","PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1","PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2","PEERDIST_STATUS_INFO","PEERDIST_STATUS_INFO structure [Peer Networking]","PPEERDIST_STATUS_INFO","PPEERDIST_STATUS_INFO structure pointer [Peer Networking]","p2p.peerdist_status_info","peerdist/PCPEERDIST_STATUS_INFO","peerdist/PEERDIST_STATUS_INFO","peerdist/PPEERDIST_STATUS_INFO"]
old-location: p2p\peerdist_status_info.htm
tech.root: p2p
ms.assetid: 6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6
ms.date: 12/05/2018
ms.keywords: '*PPEERDIST_STATUS_INFO, PCPEERDIST_STATUS_INFO, PCPEERDIST_STATUS_INFO structure pointer [Peer Networking], PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1, PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2, PEERDIST_STATUS_INFO, PEERDIST_STATUS_INFO structure [Peer Networking], PPEERDIST_STATUS_INFO, PPEERDIST_STATUS_INFO structure pointer [Peer Networking], p2p.peerdist_status_info, peerdist/PCPEERDIST_STATUS_INFO, peerdist/PEERDIST_STATUS_INFO, peerdist/PPEERDIST_STATUS_INFO'
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
targetos: Windows
req.typenames: PEERDIST_STATUS_INFO, *PPEERDIST_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peerdist_status_info_tag
 - peerdist/peerdist_status_info_tag
 - PPEERDIST_STATUS_INFO
 - peerdist/PPEERDIST_STATUS_INFO
 - PEERDIST_STATUS_INFO
 - peerdist/PEERDIST_STATUS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PEERDIST_STATUS_INFO
---

# PEERDIST_STATUS_INFO structure


## -description

The <b>PEERDIST_STATUS_INFO</b> structure contains information about the current status and capabilities of the BranchCache service on the local computer.

## -struct-fields

### -field cbSize

Size, in bytes, of the <b>PEERDIST_STATUS_INFO</b> structure.

### -field status

Specifies the current status of the BranchCache service. This member should be one of following values defined in the <a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a> enumeration.

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

<a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistgetstatusex">PeerDistGetStatusEx</a>