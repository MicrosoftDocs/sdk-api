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

# GetThemeStream function


## -description


Retrieves a data stream corresponding to a specified theme, starting from a specified part, state, and property.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to the theme from which the stream will be retrieved.


### -param iPartId [in]

Type: <b>int</b>

Specifies the part to retrieve a stream from. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Specifies the state of the part.


### -param iPropId [in]

Type: <b>int</b>

Specifies the property to retrieve.


### -param ppvStream [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">VOID</a>**</b>

Address of a pointer that receives the stream.


### -param pcbStream [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer that receives the length, in bytes, of the stream received by <i>ppvStream</i>.


### -param hInst [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

If <i>iPropId</i> is TMT_STREAM, this value is <b>NULL</b>. If <i>iPropId</i> is TMT_DISKSTREAM, this value is the HINSTANCE of a loaded styles file.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Windows 8:</b> In high contrast mode, the data stream retrieved by this function is not valid after the <i>hTheme</i> theme handle is closed.


The data stream retrieved by this function is not a copy; do not delete or close the data stream after using it.




## -see-also




<a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>
 

 

