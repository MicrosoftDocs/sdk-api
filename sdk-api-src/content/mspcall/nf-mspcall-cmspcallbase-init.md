---
UID: NF:mspcall.CMSPCallBase.Init
title: CMSPCallBase::Init
author: windows-sdk-content
description: The Init method is called by the MSP address object (in the method CreateMSPCall) to initialize the MSP call object. The derived class should initialize its members using the passed-in information.
old-location: tapi3\cmspcallbase_init.htm
tech.root: tapi
ms.assetid: bda49b8e-4ae5-4cf9-ae61-44fbf41e2cda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],Init method, CMSPCallBase.Init, CMSPCallBase::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_init, mspcall/CMSPCallBase::Init, tapi3.cmspcallbase_init
ms.topic: method
req.header: mspcall.h
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
 - Mspcall.h
api_name:
 - CMSPCallBase.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallBase::Init


## -description


The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>) to initialize the MSP call object. The derived class should initialize its members using the passed-in information.


## -parameters




### -param pMSPAddress

Pointer to MSP call object to be initialized.


### -param htCall

The MSP handle for the call.


### -param dwReserved

Reserved.


### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types of call.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726496(v=VS.85).aspx">CMSPCallBase</a>



<a href="https://msdn.microsoft.com/en-us/library/ms726574(v=VS.85).aspx">CMSPCallMultiGraph::Init</a>



<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>
 

 

