---
UID: NF:strmif.IAMVfwCompressDialogs.ShowDialog
title: IAMVfwCompressDialogs::ShowDialog method
author: windows-driver-content
description: The ShowDialog method displays the specified dialog box.
old-location: dshow\iamvfwcompressdialogs_showdialog.htm
old-project: DirectShow
ms.assetid: 4826bd47-0091-4a74-b88d-72a5b0f1c5ac
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMVfwCompressDialogs, IAMVfwCompressDialogs interface [DirectShow], ShowDialog method, IAMVfwCompressDialogs::ShowDialog, IAMVfwCompressDialogsShowDialog, ShowDialog method [DirectShow], ShowDialog method [DirectShow], IAMVfwCompressDialogs interface, ShowDialog,IAMVfwCompressDialogs.ShowDialog, dshow.iamvfwcompressdialogs_showdialog, strmif/IAMVfwCompressDialogs::ShowDialog
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVfwCompressDialogs.ShowDialog
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCompressDialogs::ShowDialog method


## -description



The <code>ShowDialog</code> method displays the specified dialog box.




## -parameters




### -param iDialog [in]

Dialog box to display. This is a member of the <a href="https://msdn.microsoft.com/b1e92603-631a-45e0-aee0-3974e3114e03">VfwCompressDialogs</a> enumeration.


### -param hwnd [in]

Handle of the dialog box's parent window.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method returns an error when asked to display a dialog box while the driver is streaming or displaying another dialog box. While the driver displays the dialog box you can't stream (pause or run) the filter.

<code>IAMVfwCompressDialogs::ShowDialog</code> calls the Video for Windows video compression manager (VCM) functions <a href="https://msdn.microsoft.com/58dbe8ff-4236-456c-8361-e7716e764f89">ICConfigure</a>, <a href="https://msdn.microsoft.com/18ec2659-8589-4a13-95ea-825a3aecbf98">ICAbout</a>, <a href="https://msdn.microsoft.com/a0e65123-5224-43a4-9a1e-28a10ecbed5c">ICQueryConfigure</a>, and <a href="https://msdn.microsoft.com/073f217f-961b-4de2-9430-5ee81379e807">ICQueryAbout</a> to display the appropriate dialog box or determine if one exists.
      


        The VfwCompressDialog_QueryConfig and VfwCompressDialog_QueryAbout members of the <a href="https://msdn.microsoft.com/b1e92603-631a-45e0-aee0-3974e3114e03">VfwCompressDialogs</a> enumeration tell you whether or not the configure dialog or about dialog is available. If passed one of these flags, the filter will return S_OK if the dialog exists, and S_FALSE if it does not. If a dialog is available, you call <code>ShowDialog</code> with the value VfwCompressDialog_Config or VfwCompressDialog_About to bring up the dialog.
      




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5cc23d68-e0e6-401a-8d16-63c8c68af241">IAMVfwCompressDialogs Interface</a>
 

 

