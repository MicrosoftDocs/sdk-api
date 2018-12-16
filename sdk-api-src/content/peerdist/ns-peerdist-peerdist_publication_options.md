---
UID: NS:peerdist.peerdist_publication_options_tag
title: PEERDIST_PUBLICATION_OPTIONS
author: windows-sdk-content
description: PEERDIST_PUBLICATION_OPTIONS structure contains publication options, including the API version information and possible option flags.
old-location: p2p\peerdist_publication_options.htm
tech.root: P2PSdk
ms.assetid: 990b6551-eaf6-47f7-bc35-ea91820f917b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPEERDIST_PUBLICATION_OPTIONS, PEERDIST_PUBLICATION_OPTIONS, PEERDIST_PUBLICATION_OPTIONS structure [Peer Networking], PPEERDIST_PUBLICATION_OPTIONS, PPEERDIST_PUBLICATION_OPTIONS structure pointer [Peer Networking], p2p.peerdist_publication_options, peerdist/PEERDIST_PUBLICATION_OPTIONS, peerdist/PPEERDIST_PUBLICATION_OPTIONS"
ms.topic: struct
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - PEERDIST_PUBLICATION_OPTIONS
product: Windows
targetos: Windows
req.typenames: PEERDIST_PUBLICATION_OPTIONS, *PPEERDIST_PUBLICATION_OPTIONS
req.redist: 
---

# PEERDIST_PUBLICATION_OPTIONS structure


## -description


The <b>PEERDIST_PUBLICATION_OPTIONS</b> structure contains publication options, including the API version information and possible option flags.


## -struct-fields




### -field dwVersion


The following possible values reflect the version number of the client:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Version 1.0

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Version 2.0

</td>
</tr>
</table>
 


### -field dwFlags

Reserved.

