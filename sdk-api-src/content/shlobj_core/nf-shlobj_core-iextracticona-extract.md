---
UID: NF:shlobj_core.IExtractIconA.Extract
title: IExtractIconA::Extract (shlobj_core.h)
author: windows-sdk-content
description: Extracts an icon image from the specified location.
old-location: shell\IExtractIcon_Extract.htm
tech.root: shell
ms.assetid: 3ce54876-e4f8-4f9a-8e1c-ec1db691f020
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Extract, Extract method [Windows Shell], Extract method [Windows Shell],IExtractIcon interface, IExtractIcon interface [Windows Shell],Extract method, IExtractIcon::Extract, IExtractIconA, IExtractIconA.Extract, IExtractIconA::Extract, IExtractIconW, IExtractIconW::Extract, _win32_IExtractIcon_Extract, shell.IExtractIcon_Extract, shlobj_core/IExtractIcon::Extract
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractIcon.Extract
 - IExtractIconA::Extract
 - IExtractIconW::Extract
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtractIconA::Extract


## -description


Extracts an icon image from the specified location.


## -parameters




### -param pszFile [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string that specifies the icon location.


### -param nIconIndex

Type: <b>UINT</b>

The index of the icon in the file pointed to by <i>pszFile</i>.


### -param phiconLarge [out, optional]

Type: <b>HICON*</b>

A pointer to an <b>HICON</b> value that receives the handle to the large icon. This parameter may be <b>NULL</b>.


### -param phiconSmall [out, optional]

Type: <b>HICON*</b>

A pointer to an <b>HICON</b> value that receives the handle to the small icon. This parameter may be <b>NULL</b>.


### -param nIconSize

Type: <b>UINT</b>

The desired size of the icon, in pixels. The low word contains the size of the large icon, and the high word contains the size of the small icon. The size specified can be the width or height. The width of an icon always equals its height.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the function extracted the icon, or S_FALSE if the calling application should extract the icon.




## -remarks



The icon location and index are the same values returned by the <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> method. If <b>IExtractIcon::Extract</b> function returns S_FALSE, these values must specify an icon file name and index that form legal parameters for a call to <a href="https://msdn.microsoft.com/a0314423-79d6-416e-8be0-be946477da3e">ExtractIcon</a>. If <b>IExtractIcon::Extract</b> does not return S_FALSE, no assumptions should be made about the meanings of the <i>pszFile</i> and <i>nIconIndex</i> parameters.




## -see-also




<a href="https://msdn.microsoft.com/f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f">IExtractIcon</a>
 

 

