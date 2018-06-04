---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PFAX_LINECALLBACK callback function


## -description


The <i>FaxLineCallback</i> function is an application-defined or library-defined callback function that the fax service calls to deliver Telephony Application Programming Interface (TAPI) events to the fax service provider (FSP).

The <b>PFAX_LINECALLBACK</b> data type is a pointer to a <i>FaxLineCallback</i> function. <i>FaxLineCallback</i> is a placeholder for an application-defined or library-defined function name.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a> function.


### -param hDevice [in]

Type: <b>DWORD</b>

Specifies a handle to either a line device or a call device. To determine whether this handle is a line handle or a call handle, use the context that the <i>dwMessage</i> parameter provides.


### -param dwMessage [in]

Type: <b>DWORD</b>

Specifies a line device or a call device message.


### -param dwInstance

Type: <b>DWORD_PTR</b>

Reserved; should not be used by the FSP.


### -param dwParam1 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message. For information about parameter values passed in this structure, see <a href="https://msdn.microsoft.com/dc11134e-6c20-426e-834e-508bf855e5da">Line Device Messages</a> in the TAPI documentation.


### -param dwParam2 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.


### -param dwParam3 [in]

Type: <b>DWORD_PTR</b>

Specifies a parameter for the message.


## -returns



This callback function does not return a value.




## -remarks



The FSP must register the <i>FaxLineCallback</i> callback function by passing its address when the fax service calls the <a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>



<a href="_tapi2_lineinitializeex">lineInitializeEx</a>
 

 

