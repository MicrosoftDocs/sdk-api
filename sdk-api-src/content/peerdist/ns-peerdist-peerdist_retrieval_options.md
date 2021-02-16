---
UID: NS:peerdist.peerdist_retrieval_options_tag
title: PEERDIST_RETRIEVAL_OPTIONS (peerdist.h)
description: The PEER_RETRIEVAL_OPTIONS structure contains version of the content information to retrieve.
helpviewer_keywords: ["*PPEERDIST_RETRIEVAL_OPTIONS","PEERDIST_RETRIEVAL_OPTIONS","PEERDIST_RETRIEVAL_OPTIONS structure [Peer Networking]","PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION","PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1","PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2","PPEERDIST_RETRIEVAL_OPTIONS","PPEERDIST_RETRIEVAL_OPTIONS structure pointer [Peer Networking]","p2p.peerdist_retrieval_options","peerdist/PEERDIST_RETRIEVAL_OPTIONS","peerdist/PPEERDIST_RETRIEVAL_OPTIONS"]
old-location: p2p\peerdist_retrieval_options.htm
tech.root: p2p
ms.assetid: cc5953bd-39cc-472e-a84b-89be7a6e6d09
ms.date: 12/05/2018
ms.keywords: '*PPEERDIST_RETRIEVAL_OPTIONS, PEERDIST_RETRIEVAL_OPTIONS, PEERDIST_RETRIEVAL_OPTIONS structure [Peer Networking], PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION, PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1, PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2, PPEERDIST_RETRIEVAL_OPTIONS, PPEERDIST_RETRIEVAL_OPTIONS structure pointer [Peer Networking], p2p.peerdist_retrieval_options, peerdist/PEERDIST_RETRIEVAL_OPTIONS, peerdist/PPEERDIST_RETRIEVAL_OPTIONS'
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
req.typenames: PEERDIST_RETRIEVAL_OPTIONS, *PPEERDIST_RETRIEVAL_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peerdist_retrieval_options_tag
 - peerdist/peerdist_retrieval_options_tag
 - PPEERDIST_RETRIEVAL_OPTIONS
 - peerdist/PPEERDIST_RETRIEVAL_OPTIONS
 - PEERDIST_RETRIEVAL_OPTIONS
 - peerdist/PEERDIST_RETRIEVAL_OPTIONS
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
 - PEERDIST_RETRIEVAL_OPTIONS
---

# PEERDIST_RETRIEVAL_OPTIONS structure


## -description

The <b>PEER_RETRIEVAL_OPTIONS</b> structure contains version  of the content information to retrieve.

## -struct-fields

### -field cbSize

Specifies the size of the input structure.

### -field dwContentInfoMinVersion

Specifies the minimum version of the content information to retrieve. Must be set to one of the following values:

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION"></a>
<a id="peerdist_retrieval_options_contentinfo_version"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1"></a>
<a id="peerdist_retrieval_options_contentinfo_version_1"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2"></a>
<a id="peerdist_retrieval_options_contentinfo_version_2"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2

### -field dwContentInfoMaxVersion

Specifies the maximum version of the content information to retrieve. Must be set to one of the following values:

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION"></a>
<a id="peerdist_retrieval_options_contentinfo_version"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1"></a>
<a id="peerdist_retrieval_options_contentinfo_version_1"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_1

<a id="PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2"></a>
<a id="peerdist_retrieval_options_contentinfo_version_2"></a>


#### PEERDIST_RETRIEVAL_OPTIONS_CONTENTINFO_VERSION_2

### -field dwReserved

Reserved. The <b>dwReserved</b> member should be set to 0.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex">PeerDistServerOpenContentInformationEx</a>