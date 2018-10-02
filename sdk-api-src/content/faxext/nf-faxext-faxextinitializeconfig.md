---
UID: NF:faxext.FaxExtInitializeConfig
title: FaxExtInitializeConfig function
author: windows-sdk-content
description: The fax service calls the FaxExtInitializeConfig function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.
old-location: fax\_mfax_faxextinitializeconfig.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxextconfigref_15lz.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxExt.h
api_name:
 - FaxExtInitializeConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxExtInitializeConfig function


## -description


The fax service calls the <b>FaxExtInitializeConfig</b> function to initialize the fax extension DLL. The service calls this function before it calls any other fax extension initialization function.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD


### -param arg5

TBD




#### - [in]

Type: <b>PFAX_EXT_GET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms684528(v=VS.85).aspx">FaxExtGetData</a> fax service callback function.


#### - pFaxExtFreeBuffer [in]

Type: <b>PFAX_EXT_FREE_BUFFER</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms684529(v=VS.85).aspx">FaxExtFreeBuffer</a> fax service callback function.


#### - pFaxExtRegisterForEvents [in]

Type: <b>PFAX_EXT_REGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms684532(v=VS.85).aspx">FaxExtRegisterForEvents</a> fax service callback function.


#### - pFaxExtSetData [in]

Type: <b>PFAX_EXT_SET_DATA</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms684530(v=VS.85).aspx">FaxExtSetData</a> fax service callback function.


#### - pFaxExtUnregisterForEvents [in]

Type: <b>PFAX_EXT_UNREGISTER_FOR_EVENTS</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms684531(v=VS.85).aspx">FaxExtUnregisterForEvents</a> fax service callback function.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, the return value is <b>NOERROR</b>.





If the fax extension DLL returns a value other than <b>NOERROR</b>, the fax service considers the extension to be in an error state. Even if other extension initialization functions succeed, the fax service does not recognize the extension.





## -remarks



A fax extension DLL must export <b>FaxExtInitializeConfig</b> if it plans to implement the fax extension configuration mechanism and receive notifications from the fax service about changes in device configuration data.

The <b>FaxExtInitializeConfig</b> function exposes pointers to the callback functions that the fax service supplies. The fax extension DLL must store these pointers in a global variable for later use.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684529(v=VS.85).aspx">FaxExtFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684528(v=VS.85).aspx">FaxExtGetData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684532(v=VS.85).aspx">FaxExtRegisterForEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684530(v=VS.85).aspx">FaxExtSetData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684531(v=VS.85).aspx">FaxExtUnregisterForEvents</a>
 

 

