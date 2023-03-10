---
UID: NF:faxdev.FaxDevShutdown
title: FaxDevShutdown function (faxdev.h)
description: The fax service calls the FaxDevShutdown function to notify the fax service provider (FSP) that the service is about to unload the FSP's DLL. FaxDevShutdown releases the global resources allocated by the FaxDevInitialize function.
helpviewer_keywords: ["FaxDevShutdown","FaxDevShutdown function [Fax Service]","_mfax_faxdevshutdown","fax._mfax_faxdevshutdown","faxdev/FaxDevShutdown"]
old-location: fax\_mfax_faxdevshutdown.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_35m6.htm
ms.date: 12/05/2018
ms.keywords: FaxDevShutdown, FaxDevShutdown function [Fax Service], _mfax_faxdevshutdown, fax._mfax_faxdevshutdown, faxdev/FaxDevShutdown
req.header: faxdev.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxDevShutdown
 - faxdev/FaxDevShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevShutdown
---

# FaxDevShutdown function


## -description

The fax service calls the <b>FaxDevShutdown</b> function to notify the fax service provider (FSP) that the service is about to unload the FSP's DLL. <b>FaxDevShutdown</b> releases the global resources allocated by the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a> function.

Exporting the <b>FaxDevShutdown</b> function is optional.



## -returns

Type: <b>HRESULT</b>

If the function succeeds, the return value is S_OK.

If the function fails, the return value is E_FAIL.

## -remarks

The fax service always unloads the FSP's DLL, even if the FSP returns failure in response to this function.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>
