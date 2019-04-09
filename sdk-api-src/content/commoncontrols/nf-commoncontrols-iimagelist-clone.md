---
UID: NF:commoncontrols.IImageList.Clone
title: IImageList::Clone (commoncontrols.h)
author: windows-sdk-content
description: Clones an existing image list.
old-location: controls\IImageList_Clone.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\clone.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Controls], Clone method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],Clone method, IImageList.Clone, IImageList::Clone, comctl_IImageList_Clone, comctl_IImageList_Clone_cpp, commoncontrols/IImageList::Clone, controls.IImageList_Clone, controls.comctl_IImageList_Clone
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
 - IImageList.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageList::Clone


## -description


Clones an existing image list.
		


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

An IID for the new image list.


### -param ppv [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PVOID</a>*</b>

The address of a  pointer to the interface for the new image list.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::Clone</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



