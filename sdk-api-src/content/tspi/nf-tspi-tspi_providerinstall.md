---
UID: NF:tspi.TSPI_providerInstall
title: TSPI_providerInstall function (tspi.h)
author: windows-sdk-content
description: The TSPI_providerInstall function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_providerInstall.
old-location: tspi\tspi_providerinstall.htm
tech.root: Tapi
ms.assetid: fb8ec97d-b96c-4533-a83e-cb9a8b4adf51
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_providerInstall, TSPI_providerInstall function [TAPI 2.2], _tspi_tspi_providerinstall, tspi.tspi_providerinstall, tspi/TSPI_providerInstall
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
 - TSPI_providerInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_providerInstall function


## -description


The 
<b>TSPI_providerInstall</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://msdn.microsoft.com/4b133336-7cd1-4af4-bc8d-4defce97559d">TUISPI_providerInstall</a>.

The 
<b>TSPI_providerInstall</b> function installs any additional "pieces" of the provider into the right directories (or at least verifying that they're there), sets up the provider's registry entries for its lines and phones, and creates any other entries necessary for the service provider. It is called from the Telephony Control Panel utility (supplied with Windows Telephony in versions 1.4 and earlier) when the 
<b>Add</b> button is pressed.


## -parameters




### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows that are required during installation.


### -param dwPermanentProviderID

The service provider's permanent provider identifier.


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM.




## -remarks



This function completes the installation of other pieces required by the service provider after its entries in the [Providers] section in the registry have been made. If the service provider requires any additional privately-defined entries in the registry for proper operation, they must also be installed. A typical way to install this section with its entries is to call 
<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a>.

This function must leave the system in a consistent state. It should run to completion, not allowing the user to abort the installation when it is partly completed. If installation fails, it is the provider's responsibility to "back out" what was done and return an error. This may imply pre-scanning to verify that a complete installation is possible, before the installation begins.

This function is called only once, during installation of the service provider, until there is a call to 
<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a>. It must be called before any other TSPI-defined function.

The Telephony Control Panel utility supplied with Windows Telephony in versions 1.4 and earlier calls this function (with external sequence requirements met as described here) when the "add" command is invoked. It does not call 
<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a> for the "add" command.

There is no corresponding function at the TAPI level. At that level, applications expect to have service providers already installed. Running applications are informed about dynamic reconfiguration through the LINEDEVSTATE_REINIT or PHONESTATE_REINIT value in the LINE_LINEDEVSTATE or PHONE_STATE message.




## -see-also




<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/b0fa2a9e-bc8b-4364-9442-2091f2366107">TSPI_providerConfig</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>



<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a>



<a href="https://msdn.microsoft.com/b13e0ed6-c053-4290-bc4c-5f66e4a376b7">TSPI_providerShutdown</a>
 

 

