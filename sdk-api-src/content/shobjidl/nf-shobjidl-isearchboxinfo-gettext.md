---
UID: NF:shobjidl.ISearchBoxInfo.GetText
title: ISearchBoxInfo::GetText
author: windows-driver-content
description: Retrieves the contents of the search box as plain text.
old-location: shell\ISearchBoxInfo_GetText.htm
old-project: shell
ms.assetid: 2bfb65d5-a27e-41f7-883e-2e1afe912586
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetText, GetText method [Windows Shell], GetText method [Windows Shell],ISearchBoxInfo interface, ISearchBoxInfo interface [Windows Shell],GetText method, ISearchBoxInfo.GetText, ISearchBoxInfo::GetText, _shell_ISearchBoxInfo_GetText, shell.ISearchBoxInfo_GetText, shobjidl/ISearchBoxInfo::GetText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	ISearchBoxInfo.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISearchBoxInfo::GetText


## -description


Retrieves the contents of the search box as plain text.


## -parameters




### -param ppsz [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the full text entered in the search box.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b2082e9-b075-488a-a6c1-f9dc99409474">ISearchBoxInfo</a>
 

 

