---
UID: NF:commctrl.HIMAGELIST_QueryInterface
title: HIMAGELIST_QueryInterface function
author: windows-sdk-content
description: Retrieves a pointer to an IImageList or IImageList2 object that corresponds to the image list's HIMAGELIST handle.
old-location: controls\HIMAGELIST_QueryInterface.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\himagelist_queryinterface.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: HIMAGELIST_QueryInterface, HIMAGELIST_QueryInterface function [Windows Controls], _shell_HIMAGELIST_QueryInterface, _shell_HIMAGELIST_QueryInterface_cpp, commctrl/HIMAGELIST_QueryInterface, controls.HIMAGELIST_QueryInterface, controls._shell_HIMAGELIST_QueryInterface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - HIMAGELIST_QueryInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HIMAGELIST_QueryInterface function


## -description


Retrieves a pointer to an <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a> or <a href="https://msdn.microsoft.com/950CA48D-A1DB-448D-B2A0-BCBD17FAC316">IImageList2</a> object that corresponds to the image list's HIMAGELIST handle.


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

The handle to the image list.


### -param riid [in]

Type: <b>REFIID</b>

The identifier of the interface being requested. Normally IID_IImageList or IID_IImageList2.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of the interface pointer requested in <i>riid</i>. If the object does not support the interface specified in <i>riid</i>, <i>ppv</i> is <b>NULL</b>.
        


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



