---
UID: NF:mfobjects.IMFMediaType.FreeRepresentation
title: IMFMediaType::FreeRepresentation method
author: windows-driver-content
description: Frees memory that was allocated by the IMFMediaType::GetRepresentation method.
old-location: mf\imfmediatype_freerepresentation.htm
old-project: medfound
ms.assetid: d2007f16-543f-4f05-a44d-b4b4ae8019fb
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: FreeRepresentation method [Media Foundation], FreeRepresentation method [Media Foundation], IMFMediaType interface, FreeRepresentation,IMFMediaType.FreeRepresentation, IMFMediaType, IMFMediaType interface [Media Foundation], FreeRepresentation method, IMFMediaType::FreeRepresentation, d2007f16-543f-4f05-a44d-b4b4ae8019fb, mf.imfmediatype_freerepresentation, mfobjects/IMFMediaType::FreeRepresentation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaType.FreeRepresentation
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaType::FreeRepresentation method


## -description



Frees memory that was allocated by the <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">IMFMediaType::GetRepresentation</a> method.




## -parameters




### -param guidRepresentation [in]


            GUID that was passed to the <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">GetRepresentation</a> method.
          


### -param pvRepresentation [in]


            Pointer to the buffer that was returned by the <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">GetRepresentation</a> method.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>
 

 

