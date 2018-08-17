---
UID: NF:faxdev.FaxDevShutdown
title: FaxDevShutdown function
author: windows-sdk-content
description: The fax service calls the FaxDevShutdown function to notify the fax service provider (FSP) that the service is about to unload the FSP's DLL. FaxDevShutdown releases the global resources allocated by the FaxDevInitialize function.
old-location: fax\_mfax_faxdevshutdown.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_35m6.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxDevShutdown, FaxDevShutdown function [Fax Service], _mfax_faxdevshutdown, fax._mfax_faxdevshutdown, faxdev/FaxDevShutdown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevShutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FaxDevShutdown function


## -description


The fax service calls the <b>FaxDevShutdown</b> function to notify the fax service provider (FSP) that the service is about to unload the FSP's DLL. <b>FaxDevShutdown</b> releases the global resources allocated by the <a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a> function.

Exporting the <b>FaxDevShutdown</b> function is optional.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the function succeeds, the return value is S_OK.

If the function fails, the return value is E_FAIL.




## -remarks



The fax service always unloads the FSP's DLL, even if the FSP returns failure in response to this function.




## -see-also




<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

