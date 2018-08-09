---
UID: NF:commoncontrols.IImageList2.Initialize
title: IImageList2::Initialize
author: windows-sdk-content
description: Initializes an image list.
old-location: controls\IImageList2_Initialize.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\initialize.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IImageList2 interface [Windows Controls],Initialize method, IImageList2.Initialize, IImageList2::Initialize, Initialize, Initialize method [Windows Controls], Initialize method [Windows Controls],IImageList2 interface, _shell_IImageList2_Initialize, _shell_IImageList2_Initialize_cpp, commoncontrols/IImageList2::Initialize, controls.IImageList2_Initialize, controls._shell_IImageList2_Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2::Initialize


## -description


Initializes an image list.


## -parameters




### -param cx [in]

Type: <b>int</b>

Width, in pixels, of each image.


### -param cy [in]

Type: <b>int</b>

Height, in pixels, of each image.


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/DFEB1934-DB7F-4151-97F9-DDB2BCCC782A">Image List Creation Flags</a>. 


### -param cInitial [in]

Type: <b>int</b>

Number of images that the image list initially contains.


### -param cGrow [in]

Type: <b>int</b>

Number of new images that the image list can contain.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



