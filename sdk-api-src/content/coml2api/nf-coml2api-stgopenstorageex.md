---
UID: NF:coml2api.StgOpenStorageEx
title: StgOpenStorageEx function (coml2api.h)
author: windows-sdk-content
description: Opens an existing root storage object in the file system. Use this function to open Compound Files and regular files.
old-location: stg\stgopenstorageex.htm
tech.root: Stg
ms.assetid: 4f2138fb-1f80-4345-a3cb-9c11023457b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StgOpenStorageEx, StgOpenStorageEx function [Structured Storage], _stg_stgopenstorageex, coml2api/StgOpenStorageEx, stg.stgopenstorageex
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - StgOpenStorageEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StgOpenStorageEx function


## -description


The <b>StgOpenStorageEx</b> function opens an existing root storage object in the file system. Use this function to open <a href="https://msdn.microsoft.com/23b425e6-dfe5-403b-8f43-de6843a03dcd">Compound Files</a> and regular files. To create a new file, use the 
<a href="https://msdn.microsoft.com/6442977d-e980-419e-abe9-9d15dbb045c1">StgCreateStorageEx</a> function.
<div class="alert"><b>Note</b>  To use enhancements, all Windows 2000, Windows XP, and Windows Server 2003 applications should call <b>StgOpenStorageEx</b>, instead of 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>. The 
<b>StgOpenStorage</b> function is used for compatibility with Windows 2000 and earlier applications.</div><div> </div>

## -parameters




### -param pwcsName [in]

A pointer to the path of the null-terminated Unicode string file that contains the storage object. This string size cannot exceed <b>MAX_PATH</b> characters.

<b>Windows Server 2003 and Windows XP/2000:  </b>Unlike the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, the <b>MAX_PATH</b> limit cannot be exceeded by using the "\\?\" prefix.


### -param grfMode [in]

A value that specifies the access mode to open the new storage object. For more information, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>. If the caller specifies transacted mode together with <b>STGM_CREATE</b> or <b>STGM_CONVERT</b>, the overwrite or conversion occurs when the commit operation is called for the root storage. If <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a> is not called for the root storage object, previous contents of the file will be restored. <b>STGM_CREATE</b> and <b>STGM_CONVERT</b> cannot be combined with the <b>STGM_NOSNAPSHOT</b> flag, because a snapshot copy is required when a file is overwritten or converted in transacted mode.

If the storage object is opened in direct mode (<b>STGM_DIRECT</b>) with access to either <b>STGM_WRITE</b> or <b>STGM_READWRITE</b>, the sharing mode must be <b>STGM_SHARE_EXCLUSIVE</b> unless the <b>STGM_DIRECT_SWMR</b> mode is specified. For more information, see the Remarks section. If the storage object is opened in direct mode with access to <b>STGM_READ</b>, the sharing mode must be either <b>STGM_SHARE_EXCLUSIVE</b> or <b>STGM_SHARE_DENY_WRITE</b>, unless <b>STGM_PRIORITY</b> or <b>STGM_DIRECT_SWMR</b> is specified. For more information, see the Remarks section.

The mode in which a file is opened can affect implementation performance. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa380364(v=VS.85).aspx">Compound File Implementation Limits</a>.


### -param stgfmt [in]

A value that specifies the storage file format. For more information, see the 
<a href="https://msdn.microsoft.com/4f070b07-9eb0-445d-818f-d6dc4d3dd0e2">STGFMT</a> enumeration.


### -param grfAttrs [in]

A value that depends upon the value of the <i>stgfmt</i> parameter. 

<b>STGFMT_DOCFILE</b> must be zero (0) or <b>FILE_FLAG_NO_BUFFERING</b>. For more information about this value, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>. If the sector size of the file, specified in <i>pStgOptions</i>, is not an integer multiple of the physical sector size of the underlying disk, then this operation will fail. All other values of <i>stgfmt</i> must be zero.


### -param pStgOptions [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/dff6e626-d0c8-4b7c-85c7-c5cb2481d810">STGOPTIONS</a> structure that contains data about the storage object opened. The <i>pStgOptions</i> parameter is valid only if the <i>stgfmt</i> parameter is set to <b>STGFMT_DOCFILE</b>. The <b>usVersion</b> member must be set before calling 
<b>StgOpenStorageEx</b>. For more information, see the <b>STGOPTIONS</b> structure.


### -param pSecurityDescriptor [in]

Reserved; must be zero.


### -param riid [in]

A value that specifies the GUID of the interface pointer to return. Can also be the header-specified value for <b>IID_IStorage</b> to obtain the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface or for <b>IID_IPropertySetStorage</b> to obtain the 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface.


### -param ppObjectOpen [out]

The address of an interface pointer variable that receives a pointer for an interface on the storage object opened; contains <b>NULL</b> if operation failed.


## -returns



This function can also return any file system errors or system errors wrapped in an <b>HRESULT</b>. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms688560(v=VS.85).aspx">Error Handling Strategies</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms693442(v=VS.85).aspx">Handling Unknown Errors</a>.




## -remarks



<b>StgOpenStorageEx</b> is a superset of the 
<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a> function, and should be used by new code. Future enhancements to  structured storage will be exposed through this function. For more information about supported platforms, see the Requirements section.

The 
<b>StgOpenStorageEx</b> function opens the specified root storage object according to the access mode in the <i>grfMode</i> parameter, and, if successful, supplies an interface pointer for the opened storage object in the <i>ppObjectOpen</i> parameter. This function can be used to obtain an <a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage compound file implementation</a>, an <a href="https://msdn.microsoft.com/de2cb778-c6eb-4487-996b-87405674f603">IPropertySetStorage compound file implementation</a>, or an  
<a href="https://msdn.microsoft.com/cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8">NTFS file system implementation of IPropertySetStorage</a>.

When you open a file, the system selects a structured storage implementation depending on which 
<a href="https://msdn.microsoft.com/4f070b07-9eb0-445d-818f-d6dc4d3dd0e2">STGFMT</a> flag you specify on the file type and on the type of drive where the file is stored.

Use the 
<b>StgOpenStorageEx</b> function to access the root storage of a structured storage document or the property set storage of any file that supports property sets. For more information about which interface identifiers (IIDs) are supported for the different 
<a href="https://msdn.microsoft.com/4f070b07-9eb0-445d-818f-d6dc4d3dd0e2">STGFMT</a> values, see 
<a href="https://msdn.microsoft.com/4f070b07-9eb0-445d-818f-d6dc4d3dd0e2">STGFMT</a>.

When a file is opened with this function to access the NTFS property set implementation, special sharing rules apply. For more information, see <a href="https://msdn.microsoft.com/cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8">IPropertySetStorage-NTFS Implementation</a>.

If a compound file is opened in transacted mode, by specifying STGM_TRANSACTED, and read-only mode, by specifying STGM_READ, it is possible to change the returned storage object. For example, it is possible to call 
<a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">IStorage::CreateStream</a>. However, it is not possible to commit those changes by calling 
<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>. Therefore, such changes will be lost.

It is not valid to use the <b>STGM_CREATE</b>, <b>STGM_DELETEONRELEASE</b>, or <b>STGM_CONVERT</b> flags in the <i>grfMode</i> parameter for this function.

To support the simple mode for saving a storage object with no substorages, the 
<b>StgOpenStorageEx</b> function accepts one of  the following two flag combinations as valid modes in the <i>grfMode</i> parameter:

<pre class="syntax" xml:space="preserve"><code>    STGM_SIMPLE | STGM_READWRITE | STGM_SHARE_EXCLUSIVE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_SIMPLE | STGM_READ | STGM_SHARE_EXCLUSIVE</code></pre>
To support the single-writer, multireader, direct mode, the first flag combination is the valid <i>grfMode</i> parameter for the writer.  The second flag combination is valid for readers.

<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT_SWMR | STGM_READWRITE | STGM_SHARE_DENY_WRITE</code></pre>
<pre class="syntax" xml:space="preserve"><code>    STGM_DIRECT_SWMR | STGM_READ | STGM_SHARE_DENY_NONE</code></pre>
For more information about simple mode and single-writer/multiple-reader modes, see 
<a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>.

<div class="alert"><b>Note</b>  Opening a transacted mode storage object in read and/or write mode without denying write permissions to others (for example, the <i>grfMode</i> parameter specifies <b>STGM_SHARE_DENY_WRITE</b>) can be time-consuming because the 
<b>StgOpenStorageEx</b> call must create a snapshot copy of the entire storage object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/23b425e6-dfe5-403b-8f43-de6843a03dcd">Compound Files</a>



<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>



<a href="https://msdn.microsoft.com/4f070b07-9eb0-445d-818f-d6dc4d3dd0e2">STGFMT</a>



<a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>



<a href="https://msdn.microsoft.com/dff6e626-d0c8-4b7c-85c7-c5cb2481d810">STGOPTIONS</a>



<a href="https://msdn.microsoft.com/3292484b-8eff-438d-b989-b58ae323872b">StgCreateDocfile</a>



<a href="https://msdn.microsoft.com/6442977d-e980-419e-abe9-9d15dbb045c1">StgCreateStorageEx</a>



<a href="https://msdn.microsoft.com/5ff18dc8-b24f-42bb-8c32-efc4d3696687">StgOpenStorage</a>
 

 

