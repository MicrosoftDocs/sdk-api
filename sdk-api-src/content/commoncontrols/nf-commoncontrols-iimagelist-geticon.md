---
UID: NF:commoncontrols.IImageList.GetIcon
title: IImageList::GetIcon
author: windows-sdk-content
description: Creates an icon from an image and a mask in an image list.
old-location: controls\IImageList_GetIcon.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\geticon.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetIcon, GetIcon method [Windows Controls], GetIcon method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetIcon method, IImageList.GetIcon, IImageList::GetIcon, comctl_IImageList_GetIcon, comctl_IImageList_GetIcon_cpp, commoncontrols/IImageList::GetIcon, controls.IImageList_GetIcon, controls.comctl_IImageList_GetIcon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.GetIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::GetIcon


## -description


Creates an icon from an image and a mask in an image list. 
		


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the image. 
				


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of flags that specify the drawing style. For a list of values, see <a href="https://msdn.microsoft.com/en-us/library/Bb761455(v=VS.85).aspx">IImageList::Draw</a>. 
				


### -param picon [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a>*</b>

A pointer to an <b>int</b> that contains the handle to the icon if successful, or <b>NULL</b> if otherwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The calling application must destroy the icon returned from this method using <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a>. 
		

To use <b>IImageList::GetIcon</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



