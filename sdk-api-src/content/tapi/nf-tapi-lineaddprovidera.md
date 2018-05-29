---
UID: NF:tapi.lineAddProviderA
title: lineAddProviderA function
author: windows-sdk-content
description: The lineAddProvider function installs a new telephony service provider into the telephony system.
old-location: tapi2\lineaddprovider.htm
old-project: Tapi
ms.assetid: d6c96dba-bbfb-4b4a-a4f5-a55fd4446f3b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_lineaddprovider, lineAddProvider, lineAddProvider function [TAPI 2.2], lineAddProviderA, lineAddProviderW, tapi/lineAddProvider, tapi/lineAddProviderA, tapi/lineAddProviderW, tapi2.lineaddprovider"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineAddProviderW (Unicode) and lineAddProviderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineAddProvider
-	lineAddProviderA
-	lineAddProviderW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineAddProviderA function


## -description


The 
<b>lineAddProvider</b> function installs a new telephony service provider into the telephony system.


## -parameters




### -param lpszProviderFilename

Pointer to a <b></b>

<b>null</b>-terminated string containing the path of the service provider to be added. 


### -param hwndOwner

Handle to a window in which any dialog boxes that need to be displayed as part of the installation process (for example, by the service provider's 
<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a> function) would be attached. Can be <b>NULL</b> to indicate that any window created during the function should have no owner window.


### -param lpdwPermanentProviderID

Pointer to a variable that receives the permanent provider identifier of the newly installed service provider.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_NOMULTIPLEINSTANCE, LINEERR_OPERATIONFAILED.




## -remarks



During this function call, TAPI checks to ensure that it can access the service provider by calling its 
<a href="https://msdn.microsoft.com/fb8ec97d-b96c-4533-a83e-cb9a8b4adf51">TSPI_providerInstall</a> function; if this is unsuccessful (if the DLL or function cannot be found, or if 
<b>TSPI_providerInstall</b> returns an error), the function fails and the provider is not added to the telephony system. If this succeeds, and the  Telephony system is active (one or more applications have called 
<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a> or 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>), TAPI does not attempt to launch the newly-added service provider. Instead, in order to activate the new service provider, TAPI issues a message to restart Windows. When the activation succeeds, applications are informed of any new devices created by way of 
<a href="https://msdn.microsoft.com/d4735eab-392f-49d9-a1d9-5895d9232624">LINE_CREATE</a> or 
<a href="https://msdn.microsoft.com/62895b10-76ce-456e-ad02-e2b7764616a8">PHONE_CREATE</a> messages, or by a 
<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a> message requesting reinitialization (if the application does not support the CREATE messages).

This function copies no files—not the service provider DLL itself nor any supporting files; the application managing the addition of the provider must ensure that the provider is installed in a directory where it can be found by TAPI (for example, \WINDOWS, \WINDOWS\SYSTEM, or elsewhere on the path).




## -see-also




<a href="https://msdn.microsoft.com/d4735eab-392f-49d9-a1d9-5895d9232624">LINE_CREATE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/62895b10-76ce-456e-ad02-e2b7764616a8">PHONE_CREATE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

