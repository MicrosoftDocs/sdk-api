---
UID: NF:tspi.TUISPI_providerInstall
title: TUISPI_providerInstall function
author: windows-sdk-content
description: Implementation of the TUISPI_providerInstall function is the service provider's opportunity to install any additional &#0034;pieces&#0034; of the provider into the right directories and set up registry entries the provider needs.
old-location: tspi\tuispi_providerinstall.htm
tech.root: tapi
ms.assetid: 4b133336-7cd1-4af4-bc8d-4defce97559d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TUISPI_providerInstall, TUISPI_providerInstall function [TAPI 2.2], _tspi_tuispi_providerinstall, tspi.tuispi_providerinstall, tspi/TUISPI_providerInstall
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
 - TUISPI_providerInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TUISPI_providerInstall function


## -description


Implementation of the 
<b>TUISPI_providerInstall</b> function is the service provider's opportunity to install any additional "pieces" of the provider into the right directories (or at least verifying that they're there) and set up registry entries the provider needs. This function makes the 
<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a> function obsolete in version 2.0 and later (supported in version 1.4 and earlier).

If the service provider requires any privately-defined entries in the registry for proper operation, they must be installed at this time.

Implementation is optional.


## -parameters




### -param lpfnUIDLLCallback

Pointer to a function the UI DLL can call to communicate with the service provider DLL to obtain information needed to display the dialog box.


### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows that are required during installation.


### -param dwPermanentProviderID

The service provider's permanent provider identifier.


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_NOMEM. LINEERR_INVALPARAM.




## -remarks



This function must leave the system in a consistent state. It should run to completion, not allowing the user to abort the installation when it is partly completed. If installation fails, it is the provider's responsibility to "back out" what was done and return an error. This may imply pre-scanning to verify that a complete installation is possible, before the installation begins.

This function can be invoked more than once during installation of the service provider, until there is a call to 
<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>. If the service provider does not require or support multiple instances of the provider, however, it returns the 
<a href="https://msdn.microsoft.com/bdaf60d1-6ff2-4bd6-b246-8556d6cae644">LINEERR_ constant</a> LINEERR_NOMULTIPLEINSTANCE.

The corresponding function at the TAPI level is 
<a href="https://msdn.microsoft.com/d6c96dba-bbfb-4b4a-a4f5-a55fd4446f3b">lineAddProvider</a>. The 
<a href="https://msdn.microsoft.com/f5256cc4-e5da-45c0-b467-c46481721227">LINE_CREATE</a> message informs applications that are running about dynamic reconfiguration.




## -see-also




<a href="https://msdn.microsoft.com/f5256cc4-e5da-45c0-b467-c46481721227">LINE_CREATE</a>



<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>



<a href="https://msdn.microsoft.com/b13e0ed6-c053-4290-bc4c-5f66e4a376b7">TSPI_providerShutdown</a>



<a href="https://msdn.microsoft.com/9730f61a-8da7-4693-9fd2-94650e36ce8a">TUISPI_providerConfig</a>



<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>
 

 

