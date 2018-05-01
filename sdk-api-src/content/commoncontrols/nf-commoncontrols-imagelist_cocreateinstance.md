---
UID: NF:commoncontrols.ImageList_CoCreateInstance
title: ImageList_CoCreateInstance function
author: windows-driver-content
description: Creates a single instance of an imagelist and returns an interface pointer to it.
old-location: controls\ImageList_CoCreateInstance.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_cocreateinstance.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ImageList_CoCreateInstance, ImageList_CoCreateInstance function [Windows Controls], _shell_ImageList_CoCreateInstance, _shell_ImageList_CoCreateInstance_cpp, commoncontrols/ImageList_CoCreateInstance, controls.ImageList_CoCreateInstance, controls._shell_ImageList_CoCreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	ImageList_CoCreateInstance
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_CoCreateInstance function


## -description


Creates a single instance of an imagelist and returns an interface pointer to it.


## -parameters




### -param rclsid [in]

Type: <b>REFCLSID</b>

A reference to the CLSID—a GUID that identifies the COM object to be created. This should be <b>CLSID_ImageList</b>.


### -param punkOuter [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the outer <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface that aggregates the object created by this function, or <b>NULL</b> if no aggregation is desired.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="https://msdn.microsoft.com/950CA48D-A1DB-448D-B2A0-BCBD17FAC316">IImageList2</a>, which provides the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this function, COM must be initialized by calling <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>.

Call <b>ImageList_CoCreateInstance</b> for a customized image list; otherwise, call <a href="https://msdn.microsoft.com/6ae80c1f-f2b7-4da9-b588-30391c8aef0e">SHGetImageList</a> to load the system image list. Call <a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a> with the <i>uflag</i> parameter set to <b>SHGFI_SYSICONINDEX</b> to retrieve a handle to the system image list.



