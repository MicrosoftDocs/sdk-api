---
UID: NF:ncryptprotect.NCryptStreamOpenToUnprotectEx
title: NCryptStreamOpenToUnprotectEx function (ncryptprotect.h)
description: Opens a stream object that can be used to decrypt large amounts of data to the same protection descriptor used for encryption.helpviewer_keywords: ["NCryptStreamOpenToUnprotectEx","NCryptStreamOpenToUnprotectEx function [Security]","ncryptprotect/NCryptStreamOpenToUnprotectEx","security.ncryptstreamopentounprotectex"]
old-location: security\ncryptstreamopentounprotectex.htm
tech.root: SecCNG
ms.assetid: 8E607F4F-4A0F-4796-8F40-D232687815AF
ms.date: 12/05/2018
ms.keywords: NCryptStreamOpenToUnprotectEx, NCryptStreamOpenToUnprotectEx function [Security], ncryptprotect/NCryptStreamOpenToUnprotectEx, security.ncryptstreamopentounprotectex
f1_keywords:
- ncryptprotect/NCryptStreamOpenToUnprotectEx
dev_langs:
- c++
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ncrypt.dll
api_name:
- NCryptStreamOpenToUnprotectEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NCryptStreamOpenToUnprotectEx function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Opens a stream object that can be used to decrypt large amounts of data to the same  protection descriptor used for encryption.Call <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> to perform the decryption. To decrypt smaller messages such as keys and passwords, call <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>.
  


## -parameters




### -param pStreamInfo [in]

A pointer to NCRYPT_PROTECT_STREAM_INFO_EX.


### -param dwFlags

Only the NCRYPT_SILENT_FLAG is supported.


### -param hWnd [in, optional]

A window handle to be used as the parent of any user
        interface that is displayed.


### -param phStream [out]

Receives a pointer to a stream handle.


## -returns



Returns a status code that indicates the success or failure of the function.
        Possible return codes include, but are not limited to:

<ul>
<li>ERROR_SUCCESS</li>
<li>NTE_INVALID_PARAMETER</li>
<li>NTE_BAD_FLAGS</li>
<li>NTE_BAD_DATA</li>
<li>NTE_NO_MEMORY</li>
<li>NTE_NOT_FOUND</li>
<li>NTE_NOT_SUPPORTED</li>
<li>NTE_INVALID_HANDLE</li>
<li>NTE_BAD_KEY</li>
<li>NTE_BAD_PROVIDER</li>
<li>NTE_BAD_TYPE</li>
<li>NTE_DECRYPTION_FAILURE</li>
</ul>


