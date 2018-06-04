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

# peerdist_retrieval_options_tag structure


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




<a href="https://msdn.microsoft.com/cba9a9e8-2397-4c78-925f-ee5d817d1ee4">PeerDistServerOpenContentInformationEx</a>
 

 

