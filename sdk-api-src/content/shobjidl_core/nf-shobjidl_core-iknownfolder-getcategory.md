---
UID: NF:shobjidl_core.IKnownFolder.GetCategory
title: IKnownFolder::GetCategory (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves the category&#8212;virtual, fixed, common, or per-user&#8212;of the selected folder.
old-location: shell\IKnownFolder_GetCategory.htm
tech.root: shell
ms.assetid: b3a7f249-9d57-4bd1-830f-1c83c745782f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCategory, GetCategory method [Windows Shell], GetCategory method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetCategory method, IKnownFolder.GetCategory, IKnownFolder::GetCategory, _shell_IKnownFolder_GetCategory, shell.IKnownFolder_GetCategory, shobjidl_core/IKnownFolder::GetCategory
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IKnownFolder.GetCategory"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolder.GetCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKnownFolder::GetCategory


## -description


Retrieves the category—virtual, fixed, common, or per-user—of the selected folder.


## -parameters




### -param pCategory [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY</a>*</b>

When this method returns, contains a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY</a> of the selected folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
 

 

