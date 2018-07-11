---
UID: NF:shobjidl.ICDBurn.Burn
title: ICDBurn::Burn
author: windows-sdk-content
description: Instructs data to be copied from the staging area to a writable CD.
old-location: shell\ICDBurn_Burn.htm
old-project: shell
ms.assetid: e081973a-e923-45de-93ba-3281be73cc93
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Burn, Burn method [Windows Shell], Burn method [Windows Shell],ICDBurn interface, ICDBurn interface [Windows Shell],Burn method, ICDBurn.Burn, ICDBurn::Burn, _shell_ICDBurn_Burn, shell.ICDBurn_Burn, shobjidl/ICDBurn::Burn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICDBurn.Burn
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# ICDBurn::Burn


## -description


Instructs data to be copied from the staging area to a writable CD.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the UI.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <i>staging area</i> has a default location of %userprofile%\Local Settings\Application Data\Microsoft\CD Burning. Its actual path can be retrieved through <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a>, <a href="https://msdn.microsoft.com/4c39fdc1-5e43-4042-8703-fb72c88e2637">SHGetSpecialFolderPath</a>, <a href="https://msdn.microsoft.com/6fcac066-1ab0-443a-9994-b68ead3bbc20">SHGetFolderLocation</a>, <a href="https://msdn.microsoft.com/10b00497-fc3b-4e34-acd8-bc0721c0dc05">SHGetSpecialFolderLocation</a>, or <a href="https://msdn.microsoft.com/7e92e136-1036-4c96-931f-6e0129fb839a">SHGetFolderPathAndSubDir</a> by using the CSIDL_CDBURN_AREA value.



