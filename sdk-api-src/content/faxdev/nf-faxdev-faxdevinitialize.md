---
UID: NF:faxdev.FaxDevInitialize
title: FaxDevInitialize function (faxdev.h)
author: windows-sdk-content
description: The fax service calls the FaxDevInitialize function each time the service starts, after it loads the fax service provider (FSP) DLL. Each FSP must export the FaxDevInitialize function.
old-location: fax\_mfax_faxdevinitialize.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_8nhh.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FaxDevInitialize, FaxDevInitialize function [Fax Service], _mfax_faxdevinitialize, fax._mfax_faxdevinitialize, faxdev/FaxDevInitialize
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevInitialize function


## -description


The fax service calls the <b>FaxDevInitialize</b> function each time the service starts, after it loads the fax service provider (FSP) DLL. Each FSP must export the <b>FaxDevInitialize</b> function.


## -parameters




### -param LineAppHandle [in]

Type: <b>HLINEAPP</b>

Specifies a handle to the fax service's registration with TAPI. For more information, see the TAPI 2.x <a href="https://msdn.microsoft.com/en-us/library/ms735983(v=VS.85).aspx">lineInitializeEx</a> function.


### -param HeapHandle [in]

Type: <b>HANDLE</b>

Specifies a handle to a heap that the FSP must use for all memory allocations.


### -param LineCallbackFunction [out]

Type: <b>PFAX_LINECALLBACK*</b>

Pointer to a variable that receives a pointer to a TAPI line callback function.


### -param FaxServiceCallback [in]

Type: <b>PFAX_SERVICE_CALLBACK</b>

Pointer to a service callback function. Although this function is not used currently, this feature is expected to be available in a future version of the fax service and will provide functionality from the fax service to the FSP.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. In this case, the current instance of the fax service does not use this FSP. All devices that this FSP supports are unable to send or receive faxes. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The FSP must respond to the <b>FaxDevInitialize</b> function by performing any necessary initialization.

The FSP must supply the <a href="https://msdn.microsoft.com/en-us/library/ms684548(v=VS.85).aspx">FaxLineCallback</a> function specified by the <i>LineCallbackFunction</i> parameter. The fax service calls this function when it needs to deliver a TAPI event to the FSP. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684538(v=VS.85).aspx">FaxDevVirtualDeviceCreation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684548(v=VS.85).aspx">FaxLineCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms735983(v=VS.85).aspx">lineInitializeEx</a>
 

 

