---
UID: NF:faxext.FaxExtInitializeConfig
title: FaxExtInitializeConfig function
author: windows-driver-content
description: The fax service calls the FaxExtInitializeConfig function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.
old-location: fax\_mfax_faxextinitializeconfig.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxextconfigref_15lz.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FaxExtInitializeConfig, FaxExtInitializeConfig function [Fax Service], _mfax_faxextinitializeconfig, fax._mfax_faxextinitializeconfig, faxext/FaxExtInitializeConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: FAX_SEND, *PFAX_SEND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	FaxExt.h
api_name:
-	FaxExtInitializeConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FaxExtInitializeConfig function


## -description


The fax service calls the <b>FaxExtInitializeConfig</b> function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.


## -parameters




### -param

TBD




#### - pFaxExtFreeBuffer [in]

Type: <b>PFAX_EXT_FREE_BUFFER</b>

Pointer to a <a href="https://msdn.microsoft.com/58a30203-b734-45fa-b502-6d97711f73e0">FaxExtFreeBuffer</a> fax service callback function.


#### - pFaxExtGetData [in]

Type: <b>PFAX_EXT_GET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a> fax service callback function.


#### - pFaxExtRegisterForEvents [in]

Type: <b>PFAX_EXT_REGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a> fax service callback function.


#### - pFaxExtSetData [in]

Type: <b>PFAX_EXT_SET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/e744ea8f-2b68-4a0a-b9ee-d83f10f078b2">FaxExtSetData</a> fax service callback function.


#### - pFaxExtUnregisterForEvents [in]

Type: <b>PFAX_EXT_UNREGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/7cab1f4c-7e2f-4510-af8a-f0aee81a044e">FaxExtUnregisterForEvents</a> fax service callback function.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, the return value is <b>NOERROR</b>.





If the fax extension DLL returns a value other than <b>NOERROR</b>, the fax service considers the extension to be in an error state. Even if other extension initialization functions succeed, the fax service does not recognize the extension.





## -remarks



A fax extension DLL must export <b>FaxExtInitializeConfig</b> if it plans to implement the fax extension configuration mechanism and receive notifications from the fax service about changes in device configuration data.

The <b>FaxExtInitializeConfig</b> function exposes pointers to the callback functions that the fax service supplies. The fax extension DLL must store these pointers in a global variable for later use.




## -see-also




<a href="https://msdn.microsoft.com/58a30203-b734-45fa-b502-6d97711f73e0">FaxExtFreeBuffer</a>



<a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a>



<a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a>



<a href="https://msdn.microsoft.com/e744ea8f-2b68-4a0a-b9ee-d83f10f078b2">FaxExtSetData</a>



<a href="https://msdn.microsoft.com/7cab1f4c-7e2f-4510-af8a-f0aee81a044e">FaxExtUnregisterForEvents</a>
 

 

