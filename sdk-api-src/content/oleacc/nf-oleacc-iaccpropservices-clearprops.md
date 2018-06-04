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

# IAccPropServices::ClearProps


## -description


Servers use <b>ClearProps</b> to restore default values to properties of accessible elements that they had previously annotated.

If servers know the <b>HWND</b> of the object they want to clear, they can use <a href="https://msdn.microsoft.com/7fd3f595-4897-481f-972e-04cf1a4c6046">IAccPropServices::ClearHwndProps</a>.


## -parameters




### -param pIDString [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Identify the accessible element that is to be un-annotated.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Length of <i>pIDString</i>.


### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specify an array of properties that is to be reset. These properties will revert to the default behavior they displayed before they were annotated.


### -param cProps [in]

Type: <b>int</b>

Size of <i>paProps</i> array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



See the support section for a list of supported properties and their expected types.

Clearing the annotation for a property will cause any associated resources to be released. If a callback property server was used (see <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>), it will be released.



