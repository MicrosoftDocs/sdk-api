---
UID: NF:coml2api.StgCreateStorageEx
title: StgCreateStorageEx function (coml2api.h)
description: Creates a new storage object using a provided implementation for the IStorage or IPropertySetStorage interfaces.
helpviewer_keywords: ["All other values of stgfmt","STGFMT_DOCFILE","StgCreateStorageEx","StgCreateStorageEx function [Structured Storage]","_stg_stgcreatestorageex","coml2api/StgCreateStorageEx","stg.stgcreatestorageex"]
old-location: stg\stgcreatestorageex.htm
tech.root: Stg
ms.assetid: 6442977d-e980-419e-abe9-9d15dbb045c1
ms.date: 12/05/2018
ms.keywords: All other values of stgfmt, STGFMT_DOCFILE, StgCreateStorageEx, StgCreateStorageEx function [Structured Storage], _stg_stgcreatestorageex, coml2api/StgCreateStorageEx, stg.stgcreatestorageex
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
 - StgCreateStorageEx
 - coml2api/StgCreateStorageEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - StgCreateStorageEx
---

# StgCreateStorageEx function


## -description

The <b>StgCreateStorageEx</b> function
			 creates a new storage object using a provided implementation for the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> or 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interfaces. To open an existing file, use the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex">StgOpenStorageEx</a> function instead.

Applications written for Windows 2000, Windows Server 2003 and Windows XP must use 
<b>StgCreateStorageEx</b> rather than 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a> to take advantage of the enhanced Windows 2000 and Windows XP  Structured Storage features.

## -parameters

### -param pwcsName [in]

A pointer to the path of the file to create. It is passed uninterpreted to the file system. This can be a relative name or <b>NULL</b>. If <b>NULL</b>, a temporary file is allocated with a unique name. If non-<b>NULL</b>, the string size must not exceed MAX_PATH characters. 




<b>Windows 2000:  </b>Unlike the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function, you cannot exceed the MAX_PATH limit by using the "\\?\" prefix.

### -param grfMode [in]

A value that specifies the access mode to use when opening the new storage object. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. If the caller specifies transacted mode together with STGM_CREATE or STGM_CONVERT, the overwrite or conversion takes place when the commit operation is called for the root storage. If <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> is not called for the root storage object, previous contents of the file will be restored. STGM_CREATE and STGM_CONVERT cannot be combined with the STGM_NOSNAPSHOT flag, because a snapshot copy is required when a file is overwritten or converted in the transacted mode.

### -param stgfmt [in]

A value that specifies the storage file format. For more information, see the 
<a href="/previous-versions/windows/desktop/legacy/aa380330(v=vs.85)">STGFMT</a> enumeration.

### -param grfAttrs [in]

A value that depends on the value of the <i>stgfmt</i> parameter.

<table>
<tr>
<th>Parameter Values</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STGFMT_DOCFILE"></a><a id="stgfmt_docfile"></a><dl>
<dt><b>STGFMT_DOCFILE</b></dt>
</dl>
</td>
<td width="60%">
0, or FILE_FLAG_NO_BUFFERING. For more information, see  
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>. If the sector size of the file, specified in <i>pStgOptions</i>, is not an integer multiple of the underlying disk's physical sector size, this operation will fail.

</td>
</tr>
<tr>
<td width="40%"><a id="All_other_values_of_stgfmt"></a><a id="all_other_values_of_stgfmt"></a><a id="ALL_OTHER_VALUES_OF_STGFMT"></a><dl>
<dt><b>All other values of <i>stgfmt</i></b></dt>
</dl>
</td>
<td width="60%">
Must be 0.

</td>
</tr>
</table>

### -param pStgOptions [in]

The <i>pStgOptions</i> parameter is valid only if the <i>stgfmt</i> parameter is set to STGFMT_DOCFILE. If the <i>stgfmt</i> parameter is set to STGFMT_DOCFILE, <i>pStgOptions</i> points to the 
<a href="/windows/desktop/api/coml2api/ns-coml2api-stgoptions">STGOPTIONS</a> structure, which specifies features of the storage object, such as the sector size. This parameter may be <b>NULL</b>, which creates a storage object with a default sector size of 512 bytes. If non-<b>NULL</b>, the <b>ulSectorSize</b> member must be set to either 512 or 4096. If set to 4096, STGM_SIMPLE may not be specified in the <i>grfMode</i> parameter. The <b>usVersion</b> member must be set before calling 
<b>StgCreateStorageEx</b>. For more information, see <b>STGOPTIONS</b>.

### -param pSecurityDescriptor [in]

Enables the ACLs to be set when the file is created. If not <b>NULL</b>, needs to be a pointer to the  <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. See <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> for information on how to set ACLs on files.

<b>Windows Server 2003, Windows 2000 Server, Windows XP and Windows 2000 Professional:  </b>Value must be <b>NULL</b>.

### -param riid [in]

A value that specifies the interface identifier (IID) of the interface pointer to return. This IID may be for the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface or the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface.

### -param ppObjectOpen [out]

A pointer to an interface pointer variable that receives a pointer for an interface on the new storage object; contains <b>NULL</b> if operation failed.

## -returns

This function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. For more information, see 
<a href="/windows/desktop/com/error-handling-strategies">Error Handling Strategies</a> and 
<a href="/windows/desktop/com/handling-unknown-errors">Handling Unknown Errors</a>.

## -remarks

When an application modifies its file, it usually creates a copy of the original. The <b>StgCreateStorageEx</b> function is one way for creating a copy. This function works indirectly with the Encrypting File System (EFS) duplication API. When you use this function, you will need to set the options for the file storage in the <a href="/windows/desktop/api/coml2api/ns-coml2api-stgoptions">STGOPTIONS</a> structure.

<b>StgCreateStorageEx</b> is a superset of the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a> function, and should be used by new code. Future enhancements to Structured Storage will be exposed through the 
<b>StgCreateStorageEx</b> function. See the following Requirements section for information on supported platforms.

The 
<b>StgCreateStorageEx</b> function creates a new storage object using one of the system-provided, structured-storage implementations. This function can be used to obtain an  
<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage compound file implementation</a>, an <a href="/windows/desktop/Stg/ipropertysetstorage-compound-file-implementation">IPropertySetStorage compound file implementation</a>, or to obtain an 
<a href="/windows/desktop/Stg/ipropertysetstorage-ntfs-file-system-implementation">IPropertySetStorage NTFS implementation</a>.

When a new file is created, the storage implementation used depends on the 
flag that you specify and on the type of drive on which the file is stored. For more information, see the 
<a href="/previous-versions/windows/desktop/legacy/aa380330(v=vs.85)">STGFMT</a> enumeration.

<b>StgCreateStorageEx</b> creates the file if it does not exist. If it does exist, the use of the STGM_CREATE, STGM_CONVERT, and STGM_FAILIFTHERE flags in the <i>grfMode</i> parameter indicate how to proceed. For more information on these values, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. It is not valid, in direct mode, to specify the STGM_READ mode in the <i>grfMode</i> parameter (direct mode is indicated by not specifying the STGM_TRANSACTED flag). This function cannot be used to open an existing file; use the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex">StgOpenStorageEx</a> function instead.

You can use the 
<b>StgCreateStorageEx</b> function to get access to the root storage of a structured-storage document or the property set storage of any file that supports property sets. See the 
<a href="/previous-versions/windows/desktop/legacy/aa380330(v=vs.85)">STGFMT</a> documentation for information about which IIDs are supported for different 
<b>STGFMT</b> values.

When a file is created with this function to access the NTFS property set implementation, special sharing rules apply. For more information, see 
<a href="/windows/desktop/Stg/ipropertysetstorage-ntfs-file-system-implementation">IPropertySetStorage-NTFS Implementation</a>.

If a compound file is created in transacted mode (by specifying STGM_TRANSACTED) and read-only mode (by specifying STGM_READ), it is possible to make changes to the returned storage object. For example, it is possible to call 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">IStorage::CreateStream</a>. However, it is not possible to commit those changes by calling 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>. Therefore, such changes will be lost.

Specifying STGM_SIMPLE provides a much faster implementation of a compound file object in a limited, but frequently used case involving applications that require a compound file implementation with multiple streams and no storages. For more information, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. It is not valid to specify that STGM_TRANSACTED if STGM_SIMPLE is specified.

The simple mode does not support all the methods on 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>. Specifically, in simple mode, supported 
<b>IStorage</b> methods are <a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">CreateStream</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">Commit</a>, and 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-setclass">SetClass</a> as well as the COM <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> methods of <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. In addition, 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-setelementtimes">SetElementTimes</a> is supported with a <b>NULL</b> name, allowing applications to set times on a root storage. All the other methods of 
<b>IStorage</b> return STG_E_INVALIDFUNCTION.

If the <i>grfMode</i> parameter specifies STGM_TRANSACTED and no file yet exists with the name specified by the <i>pwcsName</i> parameter, the file is created immediately. In an access-controlled file system, the caller must have write permissions for the file system directory in which the compound file is created. If STGM_TRANSACTED is not specified, and STGM_CREATE is specified, an existing file with the same name is destroyed before creating the new file.

You can also use 
<b>StgCreateStorageEx</b> to create a temporary compound file by passing a <b>NULL</b> value for the <i>pwcsName</i> parameter. However, these files are temporary only in the sense that they have a unique system-provided name – one that is probably meaningless to the user. The caller is responsible for deleting the temporary file when finished with it, unless STGM_DELETEONRELEASE was specified for the <i>grfMode</i> parameter. For more information on these flags, see 
<a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/previous-versions/windows/desktop/legacy/aa380330(v=vs.85)">STGFMT</a>



<a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>



<a href="/windows/desktop/api/coml2api/ns-coml2api-stgoptions">STGOPTIONS</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes">StgCreateDocFileOnILockBytes</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile">StgCreateDocfile</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex">StgOpenStorageEx</a>