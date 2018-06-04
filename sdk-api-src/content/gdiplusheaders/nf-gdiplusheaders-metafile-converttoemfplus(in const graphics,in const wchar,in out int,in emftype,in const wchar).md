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

# Metafile::ConvertToEmfPlus(IN const Graphics,IN const WCHAR,IN OUT INT,IN EmfType,IN const WCHAR)


## -description


The <b>Metafile::ConvertToEmfPlus</b> method converts this <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object to the EMF+ format.


## -parameters




### -param refGraphics [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object whose state (settings for antialiasing, interpolation, and the like) is applied to the records stored in the converted metafile.


### -param filename




### -param conversionFailureFlag




### -param emfType [in]

Type: <b><a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a> enumeration that specifies whether the converted file has the <b>EmfTypeEmfPlusOnly</b> format or the <b>EmfTypeEmfPlusDual</b> format. Do not pass <b>EmfTypeEmfOnly</b>. The default value is <b>EmfTypeEmfPlusOnly</b>.


### -param description [in]

Type: <b>const WCHAR*</b>

Optional. Pointer to a null-terminated wide-character string that is stored in the header of the converted metafile. The default value is <b>NULL</b>.


#### - conversionSuccess [out]

Type: <b>BOOL*</b>

Optional. Pointer to a <b>BOOL</b> that receives <b>TRUE</b> if all the metafile records were converted successfully; <b>FALSE</b> otherwise. Pass <b>NULL</b> if you do not want to receive this information. The default value is <b>NULL</b>.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns OK, which is an element of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



This method replaces the records originally in the <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object with the converted records. To retain a copy of the original <b>Metafile</b> object, call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a> method.

If you set the <i>emfType</i> parameter to <b>EmfTypeEmfPlusDual</b>, the converted metafile contains an Enhanced Metafile (EMF) representation and an EMF+ representation. The EMF representation is the original set of EMF records rather than EMF records converted back from the newly created EMF+ records.

It is possible for the return value to be <b>Ok</b> and the value returned in <i>conversionSuccess</i> to be <b>FALSE</b>. Sometimes the overall conversion is considered to be successful even if a few individual records failed to convert with complete accuracy. For example, the original metafile might have records or operations that are not supported by Windows GDI+ (or EMF+), in which case those records or operations are emulated.



