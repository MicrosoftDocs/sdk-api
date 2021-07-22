---
UID: NF:shobjidl_core.IFileOperation.NewItem
title: IFileOperation::NewItem (shobjidl_core.h)
description: Declares a new item that is to be created in a specified location.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","NewItem method","IFileOperation.NewItem","IFileOperation::NewItem","NewItem","NewItem method [Windows Shell]","NewItem method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_NewItem","shell.IFileOperation_NewItem","shobjidl_core/IFileOperation::NewItem"]
old-location: shell\IFileOperation_NewItem.htm
tech.root: shell
ms.assetid: 810a1275-cae2-4487-b517-22aa8e4374a9
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],NewItem method, IFileOperation.NewItem, IFileOperation::NewItem, NewItem, NewItem method [Windows Shell], NewItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_NewItem, shell.IFileOperation_NewItem, shobjidl_core/IFileOperation::NewItem
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperation::NewItem
 - shobjidl_core/IFileOperation::NewItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperation.NewItem
---

# IFileOperation::NewItem


## -description

Declares a new item that is to be created in a specified location.

## -parameters

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder that will contain the new item.

### -param dwFileAttributes [in]

Type: <b>DWORD</b>

A bitwise value that specifies the file system attributes for the file or folder. See <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> for possible values.

### -param pszName [in]

Type: <b>LPCWSTR</b>

Pointer to the file name of the new item, for instance <b>Newfile.txt</b>. This is a null-terminated, Unicode string.

### -param pszTemplateName [in]

Type: <b>LPCWSTR</b>

Pointer to the name of the template file (for example <b>Excel9.xls</b>) that the new item is based on, stored in one of the following locations:
                    
                    

<ul>
<li>CSIDL_COMMON_TEMPLATES. The default path for this folder is %ALLUSERSPROFILE%\Templates.</li>
<li>CSIDL_TEMPLATES. The default path for this folder is %USERPROFILE%\Templates.</li>
<li>%SystemRoot%\shellnew</li>
</ul>
This is a null-terminated, Unicode string used to specify an existing file of the same type as the new file, containing the minimal content that an application wants to include in any new file.

This parameter is normally <b>NULL</b> to specify a new, blank file.

### -param pfopsItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for status and failure notifications. If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the creation operation are included there, so set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not create the new item, it merely declares the item to be created. To create a new item, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::NewItem</b> to declare the specifics of the new file or folder.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to create the new item.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-postnewitem">PostNewItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-prenewitem">PreNewItem</a>