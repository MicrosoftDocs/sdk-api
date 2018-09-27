---
UID: NF:tspi.TUISPI_providerConfig
title: TUISPI_providerConfig function
author: windows-sdk-content
description: The TUISPI_providerConfig function implements the UI elements that must execute in the context of the calling application. This function makes the TSPI_providerConfig function obsolete in version 2.0 and later (supported in version 1.4 and earlier).
old-location: tspi\tuispi_providerconfig.htm
tech.root: tapi
ms.assetid: 9730f61a-8da7-4693-9fd2-94650e36ce8a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: TUISPI_providerConfig, TUISPI_providerConfig function [TAPI 2.2], _tspi_tuispi_providerconfig, tspi.tuispi_providerconfig, tspi/TUISPI_providerConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
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
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TUISPI_providerConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TUISPI_providerConfig function


## -description


The 
<b>TUISPI_providerConfig</b> function implements the UI elements that must execute in the context of the calling application. This function makes the 
<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

The 
<b>TUISPI_providerConfig</b> function gathers configuration information from the user. It can use a dialog box, and this dialog box can include sub-dialog boxes associated with other APIs (such as Comm/datamodem) for the setup of specific devices.

Implementation is optional.


## -parameters




### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box and to send updated configuration to the service provider.


### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows required during the configuration.


### -param dwPermanentProviderID

The service provider's permanent provider identifier.


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_NOMEM.




## -remarks



This function may be called while the service provider is in use (that is, between calls of 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a> and 
<a href="https://msdn.microsoft.com/b13e0ed6-c053-4290-bc4c-5f66e4a376b7">TSPI_providerShutdown</a>).

Any changes that affect the behavior visible through TSPI should take effect only when the service provider is restarted at the next 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>.

There is no directly corresponding function at the TAPI level. In TAPI, applications have access to the functions 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a> and 
<a href="https://msdn.microsoft.com/64f2626a-283d-47c8-aecd-57d31712a700">phoneConfigDialog</a>, which allow configuration of parameters of a particular line or phone once it has been installed.




## -see-also




<a href="https://msdn.microsoft.com/405af7aa-eb0b-49a1-9712-2f86357fc720">TUISPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/6bdd4206-0028-43f0-8da8-2fc11779f7d2">TUISPI_phoneConfigDialog</a>



<a href="https://msdn.microsoft.com/4b133336-7cd1-4af4-bc8d-4defce97559d">TUISPI_providerInstall</a>



<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>
 

 

