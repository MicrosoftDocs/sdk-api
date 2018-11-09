---
UID: NF:tspi.TSPI_providerConfig
title: TSPI_providerConfig function
author: windows-sdk-content
description: The TSPI_providerConfig function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement TUISPI_providerConfig.
old-location: tspi\tspi_providerconfig.htm
tech.root: tapi
ms.assetid: b0fa2a9e-bc8b-4364-9442-2091f2366107
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: TSPI_providerConfig, TSPI_providerConfig function [TAPI 2.2], _tspi_tspi_providerconfig, tspi.tspi_providerconfig, tspi/TSPI_providerConfig
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
 - TSPI_providerConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_providerConfig function


## -description


The 
<b>TSPI_providerConfig</b> function is obsolete. TAPI version 1.4 or earlier service providers can implement this TSPI function. TAPI version 2.0 or later TSPs implement 
<a href="https://msdn.microsoft.com/9730f61a-8da7-4693-9fd2-94650e36ce8a">TUISPI_providerConfig</a>.

The 
<b>TSPI_providerConfig</b> function gathers configuration information from the user. It may use a dialog box, and this dialog box can include sub-dialog boxes associated with other APIs (such as Comm/datamodem) for the setup of specific devices.


## -parameters




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

The Telephony Control Panel utility supplied with Windows Telephony in versions 1.4 and earlier calls this function when the setup command is invoked.

There is no directly corresponding function at the TAPI level. In TAPI, applications have access to the functions 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a> and 
<a href="https://msdn.microsoft.com/64f2626a-283d-47c8-aecd-57d31712a700">phoneConfigDialog</a>, which allow configuration of parameters of a particular line or phone once it has been installed.




## -see-also




<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/cce9460c-0914-4f02-a6a4-efb7f43ed22a">TSPI_phoneConfigDialog</a>



<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a>



<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a>



<a href="https://msdn.microsoft.com/9730f61a-8da7-4693-9fd2-94650e36ce8a">TUISPI_providerConfig</a>
 

 

