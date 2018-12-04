---
UID: NF:tspi.TSPI_providerRemove
title: TSPI_providerRemove function
author: windows-sdk-content
description: The TSPI_providerRemove function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_providerRemove.
old-location: tspi\tspi_providerremove.htm
tech.root: tapi
ms.assetid: 3d6c6183-d5ab-4939-8f44-dfc42458706f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: TSPI_providerRemove, TSPI_providerRemove function [TAPI 2.2], _tspi_tspi_providerremove, tspi.tspi_providerremove, tspi/TSPI_providerRemove
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
 - TSPI_providerRemove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_providerRemove function


## -description


The 
<b>TSPI_providerRemove</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://msdn.microsoft.com/217d1f40-7f3f-49a0-b29e-e2da85ba47f1">TUISPI_providerRemove</a>.

The 
<b>TSPI_providerRemove</b> function asks the user to confirm elimination of the service provider. It is the responsibility of the service provider to remove any registry entries that the service provider added at <b>addProvider</b> time, as well as any other modules and files that are no longer needed.


## -parameters




### -param hwndOwner

The handle of the parent window in which the function can create any dialog box windows required during the removal.


### -param dwPermanentProviderID

The service provider's permanent provider identifier.


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM.




## -remarks



This function must guarantee that the service provider's section and privately-defined information for the service provider is removed from the registry if it returns success. In particular, the [Provider&lt;PPID&gt;] section whose &lt;PPID&gt; matches <i>dwPermanentProviderID</i> must be removed, including its <i>NumLines</i> and <i>NumPhones</i> entries. If the function returns success, it is the caller's responsibility to remove the matching <i>ProviderIDx</i> and <i>ProviderFilenamex</i> entries from the [Providers] section, and renumber the remaining entries in the [Providers] section accordingly.

This procedure must leave the system in a consistent state. It should run to completion, not allowing the user to abort the removal when it is partly completed. If removal fails, it is the provider's responsibility to "back out" what was done and return an error. This may imply pre-scanning to verify that a complete removal is possible, before the removal begins.

This function can be called while the service provider is in use (that is, between 
<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a> and 
<a href="https://msdn.microsoft.com/b13e0ed6-c053-4290-bc4c-5f66e4a376b7">TSPI_providerShutdown</a>). If this happens, the service provider should do an appropriate combination of displaying a user dialog box to announce any conflict and confirm removal, restricting removal options to those that can be performed transparently, or issuing 
<a href="https://msdn.microsoft.com/0344151e-3f40-472d-84c2-906291777da6">LINE_CLOSE</a> and 
<a href="https://msdn.microsoft.com/ac9e736c-508b-4048-a958-708264e8045e">PHONE_CLOSE</a> messages to inform TAPI and applications that the affected devices have been forcibly closed for removal. In any case, any changes that affect the behavior visible through TSPI should take effect only when the service provider is shut down at the next 
<b>TSPI_providerShutdown</b>.

This function should not return LINEERR_INUSE or other errors that might occur because the provider is in use by an application; instead, the provider should confer with the user directly about this problem, and then return LINEERR_OPERATIONFAILED if the user decides to abort the operation.

This procedure is called only once, at the time of removal of the service provider, until there is a call to 
<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a>. It is the responsibility of the caller to ensure this.

The Telephony Control Panel utility supplied with Windows Telephony in versions 1.4 and earlier calls this function (with external sequence requirements met as described here) when the "remove" command is invoked.

There is no corresponding function at the TAPI level. At that level, applications expect to have service providers already installed; otherwise their lines and phones do not appear within the available sequence of device identifiers. Running applications are informed about dynamic reconfiguration, including removal of service providers, through the LINEDEVSTATE_REINIT or PHONESTATE_REINIT value in the LINE_LINEDEVSTATE or PHONE_STATE message.




## -see-also




<a href="https://msdn.microsoft.com/0344151e-3f40-472d-84c2-906291777da6">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/6e59a7a7-660c-493f-ae0f-0c46a446c4be">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/ac9e736c-508b-4048-a958-708264e8045e">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/6cb7817b-6df3-4a6a-a666-b41c2eb0b118">TSPI_providerInit</a>



<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a>



<a href="https://msdn.microsoft.com/b13e0ed6-c053-4290-bc4c-5f66e4a376b7">TSPI_providerShutdown</a>
 

 

