---
UID: NF:coml2api.StgCreateDocfile
title: StgCreateDocfile function (coml2api.h)
description: Creates a new compound file storage object using the COM-provided compound file implementation for the IStorage interface.
helpviewer_keywords: ["StgCreateDocfile","StgCreateDocfile function [Structured Storage]","_stg_stgcreatedocfile","coml2api/StgCreateDocfile","stg.stgcreatedocfile"]
old-location: stg\stgcreatedocfile.htm
tech.root: Stg
ms.assetid: 3292484b-8eff-438d-b989-b58ae323872b
ms.date: 12/05/2018
ms.keywords: StgCreateDocfile, StgCreateDocfile function [Structured Storage], _stg_stgcreatedocfile, coml2api/StgCreateDocfile, stg.stgcreatedocfile
req.header: coml2api.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - StgCreateDocfile
 - coml2api/StgCreateDocfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - StgCreateDocfile
---

# StgCreateDocfile function


## -description

The <b>StgCreateDocfile</b> function creates a new compound file storage object using the COM-provided <a href="/windows/desktop/Stg/istorage-compound-file-implementation">compound file implementation</a> for the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface.
<div class="alert"><b>Note</b>  Applications should use the new function, 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a>, instead of 
<b>StgCreateDocfile</b>, to take advantage of enhanced  Structured Storage features. This function, 
<b>StgCreateDocfile</b>, still exists for compatibility with Windows 2000.</div><div> </div>

## -parameters

### -param pwcsName [in]

A pointer to a null-terminated Unicode string name for the compound file being created. It is passed uninterpreted to the file system. This can be a relative name or <b>NULL</b>. If <b>NULL</b>, a temporary compound file is allocated with a unique name.

### -param grfMode [in]

Specifies the access mode to use when opening the new storage object. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. If the caller specifies transacted mode together with STGM_CREATE or STGM_CONVERT, the overwrite or conversion takes place when the commit operation is called for the root storage. If <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> is not called for the root storage object, previous contents of the file will be restored. STGM_CREATE and STGM_CONVERT cannot be combined with the STGM_NOSNAPSHOT flag, because a snapshot copy is required when a file is overwritten or converted in the transacted mode.

### -param reserved [in]

Reserved for future use; must be zero.

### -param ppstgOpen [out]

A pointer to the location of the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the new storage object.

## -returns

<b>StgCreateDocfile</b> can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. For more information, see 
<a href="/windows/desktop/com/error-handling-strategies">Error Handling Strategies</a> and 
<a href="/windows/desktop/com/handling-unknown-errors">Handling Unknown Errors</a>.

## -remarks

The 
<b>StgCreateDocfile</b> function creates a new storage object using the COM-provided, compound-file implementation for the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface. The name of the open compound file can be retrieved by calling the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method.

<b>StgCreateDocfile</b> creates the file if it does not exist. If it does exist, the use of the STGM_CREATE, STGM_CONVERT, and STGM_FAILIFTHERE flags in the <i>grfMode</i> parameter indicate how to proceed. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>.

If the compound file is opened in transacted mode (the <i>grfMode</i> parameter specifies STGM_TRANSACTED) and a file with this name already exists, the existing file is not altered until all outstanding changes are committed. If the calling process lacks write access to the existing file (because of access control in the file system), the <i>grfMode</i> parameter can only specify STGM_READ and not STGM_WRITE or STGM_READWRITE. The resulting new open compound file can still be written to, but a subsequent commit operation will fail (in transacted mode, write permissions are enforced at commit time).

Specifying STGM_SIMPLE provides a much faster implementation of a compound file object in a limited, but frequently used case. This can be used by applications that require a compound-file implementation with multiple streams and no storages. The simple mode does not support all of the methods on 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>.

If the <i>grfMode</i> parameter specifies STGM_TRANSACTED and no file yet exists with the name specified by the <i>pwcsName</i> parameter, the file is created immediately. In an access-controlled file system, the caller must have write permissions in the file system directory in which the compound file is created. If STGM_TRANSACTED is not specified, and STGM_CREATE is specified, an existing file with the same name is destroyed before the new file is created.

<b>StgCreateDocfile</b> can be used to create a temporary compound file by passing a <b>NULL</b> value for the <i>pwcsName</i> parameter. However, these files are temporary only in the sense that they have a system-provided unique name — likely one that is meaningless to the user. The caller is responsible for deleting the temporary file when finished with it, unless STGM_DELETEONRELEASE was specified for the <i>grfMode</i> parameter.

## -see-also

<a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocFileOnILockBytes</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex">StgCreateStorageEx</a>