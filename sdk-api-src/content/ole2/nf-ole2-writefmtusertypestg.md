---
UID: NF:ole2.WriteFmtUserTypeStg
title: WriteFmtUserTypeStg function (ole2.h)
description: The WriteFmtUserTypeStg function writes a clipboard format and user type to the storage object.
helpviewer_keywords: ["WriteFmtUserTypeStg","WriteFmtUserTypeStg function [Structured Storage]","_stg_writefmtusertypestg","ole2/WriteFmtUserTypeStg","stg.writefmtusertypestg"]
old-location: stg\writefmtusertypestg.htm
tech.root: Stg
ms.assetid: ef60493c-164e-4633-a248-05c4afade937
ms.date: 12/05/2018
ms.keywords: WriteFmtUserTypeStg, WriteFmtUserTypeStg function [Structured Storage], _stg_writefmtusertypestg, ole2/WriteFmtUserTypeStg, stg.writefmtusertypestg
req.header: ole2.h
req.include-header: 
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WriteFmtUserTypeStg
 - ole2/WriteFmtUserTypeStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - WriteFmtUserTypeStg
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# WriteFmtUserTypeStg function


## -description

The <b>WriteFmtUserTypeStg</b> function writes a clipboard format and user type to the storage object.

## -parameters

### -param pstg [in]

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the storage object where the information is to be written.

### -param cf [in]

Specifies the clipboard format that describes the structure of the native area of the storage object. The format tag includes the policy for the names of streams and substorages within this storage object and the rules for interpreting data within those streams.

### -param lpszUserType [in]

Pointer to a null-terminated Unicode string that specifies the object's current user type. The user type value, itself, cannot be <b>NULL</b>. This is the type returned by the 
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a> method. If this function is transported to a remote machine where the object class does not exist, this persistently stored user type can be shown to the user in dialog boxes.

## -returns

This function returns HRESULT.

## -remarks

The 
<b>WriteFmtUserTypeStg</b> function must be called in an object's implementation of the 
<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method. It must also be called by document-level objects that use structured storage for their persistent representation in their save sequence.

To read the information saved, applications call the 
<a href="/windows/desktop/api/ole2/nf-ole2-readfmtusertypestg">ReadFmtUserTypeStg</a> function.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a>



<a href="/windows/desktop/api/ole2/nf-ole2-readfmtusertypestg">ReadFmtUserTypeStg</a>
