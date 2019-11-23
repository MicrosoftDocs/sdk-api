---
UID: NF:shobjidl_core.IKnownFolder.GetId
title: IKnownFolder::GetId (shobjidl_core.h)

description: Gets the ID of the selected folder.
old-location: shell\IKnownFolder_GetId.htm
tech.root: shell
ms.assetid: c20fc32f-394d-4fbe-b7dd-072d84be2713

ms.date: 12/05/2018
ms.keywords: GetId, GetId method [Windows Shell], GetId method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetId method, IKnownFolder.GetId, IKnownFolder::GetId, _shell_IKnownFolder_GetId, shell.IKnownFolder_GetId, shobjidl_core/IKnownFolder::GetId
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IKnownFolder.GetId"
dev_langs:
 - c++
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
 - IKnownFolder.GetId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKnownFolder::GetId


## -description


Gets the ID of the selected folder.


## -parameters




### -param pkfid [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>*</b>

When this method returns, returns the <a href="https://docs.microsoft.com/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> value of the known folder. Note, <b>KNOWNFOLDERID</b> values are GUIDs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
 

 

