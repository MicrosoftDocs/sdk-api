---
UID: NF:mspaddr.ShutdownMSPCallHelper
title: ShutdownMSPCallHelper function
author: windows-sdk-content
description: The ShutdownMSPCallHelper helper template function is called in the derived class' implementation of ShutdownMSPCall.
old-location: tapi3\cmspaddress_shutdownmspcallhelper.htm
tech.root: Tapi
ms.assetid: 66f7b743-6100-45b9-98b0-3bacfcffed15
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPAddress object [TAPI 2.2],ShutdownMSPCallHelper method, CMSPAddress,ShutdownMSPCallHelper, CMSPAddress.ShutdownMSPCallHelper, ShutdownMSPCallHelper, ShutdownMSPCallHelper method [TAPI 2.2], ShutdownMSPCallHelper method [TAPI 2.2],CMSPAddress object, ShutdownMSPCallHelper,CMSPAddress, _tapi3_cmspaddress_shutdownmspcallhelper, tapi3.cmspaddress_shutdownmspcallhelper
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
 - CMSPAddress.ShutdownMSPCallHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ShutdownMSPCallHelper function


## -description


The 
<b>ShutdownMSPCallHelper</b> helper template function is called in the derived class' implementation of 
<a href="https://msdn.microsoft.com/6527db85-cad8-4b0d-977a-9ab8b047e44e">ShutdownMSPCall</a>. It manipulates the passed-in aggregated TAPI call object Unknown pointer via dynamic casts to obtain a pointer to the inner MSP call object, and then calls the 
<a href="https://msdn.microsoft.com/877691cb-b12b-4389-b93c-4ff13a52f4d7">Shutdown</a> method on the MSP call object (see below).


## -parameters




### -param pUnknown

Pointer to IUnknown on aggregated TAPI call object.


### -param ppCMSPCall

Pointer to templated MSP call class, type implementation dependent.


### -param arg3

TBD




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726419(v=VS.85).aspx">CMSPAddress</a>
 

 

