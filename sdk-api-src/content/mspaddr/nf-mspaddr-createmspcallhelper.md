---
UID: NF:mspaddr.CreateMSPCallHelper
title: CreateMSPCallHelper function (mspaddr.h)
author: windows-sdk-content
description: The CreateMSPCallHelper helper template function is called in the derived class' implementation of CreateMSPCall.
old-location: tapi3\cmspaddress_createmspcallhelper.htm
tech.root: Tapi
ms.assetid: 1e894d26-de19-4c24-b4e6-58c0b4c9d5ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPAddress object [TAPI 2.2],CreateMSPCallHelper method, CMSPAddress.CreateMSPCallHelper, CreateMSPCallHelper, CreateMSPCallHelper method [TAPI 2.2], CreateMSPCallHelper method [TAPI 2.2],CMSPAddress object, _tapi3_cmspaddress_createmspcallhelper, tapi3.cmspaddress_createmspcallhelper
ms.topic: function
req.header: mspaddr.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.CreateMSPCallHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateMSPCallHelper function


## -description


The 
<b>CreateMSPCallHelper</b> helper template function is called in the derived class' implementation of 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>. It checks all of the arguments for validity, including the media type argument (via the address object method 
<a href="https://msdn.microsoft.com/en-us/library/ms726439(v=VS.85).aspx">IsValidSetOfMediaTypes</a>; see above). It sets up the aggregation between the MSP call object and the TAPI call object using the <b>CComAggObject</b> ATL class template. It then calls the 
<a href="https://msdn.microsoft.com/en-us/library/ms726510(v=VS.85).aspx">Init</a> method on the MSP call object.


## -parameters




### -param pCMSPAddress

Pointer to 
<a href="https://msdn.microsoft.com/en-us/library/ms726419(v=VS.85).aspx">CMSPAddress</a> interface for call.


### -param htCall

Handle for MSP.


### -param dwReserved

Reserved parameter, not currently used.


### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media types</a> desired for call.


### -param pOuterUnknown

Pointer to <b>IUnknown</b> interface for TAPI call object.


### -param ppMSPCall

Pointer to <b>IUnknown</b> interface for MSP call object.


### -param ppCMSPCall

Pointer to templated MSP call class, type implementation dependent.


### -param arg8

TBD




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726419(v=VS.85).aspx">CMSPAddress</a>



<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>
 

 

