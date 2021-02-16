---
UID: NF:objidl.IPersistFile.SaveCompleted
title: IPersistFile::SaveCompleted (objidl.h)
description: Notifies the object that it can write to its file.
helpviewer_keywords: ["IPersistFile interface [COM]","SaveCompleted method","IPersistFile.SaveCompleted","IPersistFile::SaveCompleted","SaveCompleted","SaveCompleted method [COM]","SaveCompleted method [COM]","IPersistFile interface","_com_ipersistfile_savecompleted","com.ipersistfile_savecompleted","objidl/IPersistFile::SaveCompleted"]
old-location: com\ipersistfile_savecompleted.htm
tech.root: com
ms.assetid: eda29981-0c24-409a-8fb9-2dc2eb96d108
ms.date: 12/05/2018
ms.keywords: IPersistFile interface [COM],SaveCompleted method, IPersistFile.SaveCompleted, IPersistFile::SaveCompleted, SaveCompleted, SaveCompleted method [COM], SaveCompleted method [COM],IPersistFile interface, _com_ipersistfile_savecompleted, com.ipersistfile_savecompleted, objidl/IPersistFile::SaveCompleted
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistFile::SaveCompleted
 - objidl/IPersistFile::SaveCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistFile.SaveCompleted
---

# IPersistFile::SaveCompleted


## -description

Notifies the object that it can write to its file. It does this by notifying the object that it can revert from NoScribble mode (in which it must not write to its file), to Normal mode (in which it can). The component enters NoScribble mode when it receives an <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> call.

## -parameters

### -param pszFileName [in]

The absolute path of the file where the object was saved previously.

## -returns

This method always returns S_OK.

## -remarks

<b>SaveCompleted</b> is called when a call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> is completed, and the file that was saved is now the current working file (having been saved with <b>Save</b> or <b>Save As</b> operations). The call to <b>Save</b> puts the object into NoScribble mode so it cannot write to its file. When <b>SaveCompleted</b> is called, the object reverts to Normal mode, in which it is free to write to its file.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
OLE does not call the <b>SaveCompleted</b> method. Typically, applications would not call it unless they are saving objects directly to files, an operation which is generally left to the end-user.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>