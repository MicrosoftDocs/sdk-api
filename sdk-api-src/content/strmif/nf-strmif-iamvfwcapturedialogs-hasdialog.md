---
UID: NF:strmif.IAMVfwCaptureDialogs.HasDialog
title: IAMVfwCaptureDialogs::HasDialog
author: windows-sdk-content
description: The HasDialog method determines if the specified dialog box exists in the driver.
old-location: dshow\iamvfwcapturedialogs_hasdialog.htm
tech.root: DirectShow
ms.assetid: be2d9b1f-c53f-4a75-89ab-ec07c655cbea
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: HasDialog, HasDialog method [DirectShow], HasDialog method [DirectShow],IAMVfwCaptureDialogs interface, IAMVfwCaptureDialogs interface [DirectShow],HasDialog method, IAMVfwCaptureDialogs.HasDialog, IAMVfwCaptureDialogs::HasDialog, IAMVfwCaptureDialogsHasDialog, dshow.iamvfwcapturedialogs_hasdialog, strmif/IAMVfwCaptureDialogs::HasDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCaptureDialogs.HasDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVfwCaptureDialogs::HasDialog


## -description



The <code>HasDialog</code> method determines if the specified dialog box exists in the driver.




## -parameters




### -param iDialog [in]

Desired dialog box. This is a member of the <a href="https://msdn.microsoft.com/0465d887-6452-4a67-9f52-a459620d12d2">VfwCaptureDialogs</a> enumeration.


## -returns



Returns S_OK if the driver contains the dialog box or S_FALSE otherwise.




## -remarks



This method calls the Video for Windows <b>videoDialog</b> function to query for the existence of the appropriate dialog box.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5198c80c-28f3-4b5c-9b3b-aa502bf3a384">IAMVfwCaptureDialogs Interface</a>
 

 

