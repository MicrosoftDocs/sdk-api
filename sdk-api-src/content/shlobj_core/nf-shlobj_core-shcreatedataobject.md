---
UID: NF:shlobj_core.SHCreateDataObject
title: SHCreateDataObject function
author: windows-sdk-content
description: Creates a data object in a parent folder.
old-location: shell\SHCreateDataObject.htm
tech.root: shell
ms.assetid: d56cdafe-9463-43a5-8ef0-6cfaf0c524a8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: SHCreateDataObject, SHCreateDataObject function [Windows Shell], _shell_SHCreateDataObject, shell.SHCreateDataObject, shlobj_core/SHCreateDataObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Dataobject-L1-1-0.dll
api_name:
 - SHCreateDataObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateDataObject function


## -description


Creates a data object in a parent folder.


## -parameters




### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> (PIDL) of the parent folder that contains the data object.


### -param cidl [in]

Type: <b>UINT</b>

The number of file objects or subfolders specified in the <i>apidl</i> parameter.


### -param apidl [in, optional]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

An array of pointers to constant <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structures, each of which uniquely identifies a file object or subfolder relative to the parent folder. Each item identifier list must contain exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure followed by a terminating zero.


### -param pdtInner [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to interface <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>. This parameter can be <b>NULL</b>. Specify <i>pdtInner</i> only if the data object created needs to support additional <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>  clipboard formats beyond the default formats it is assigned at creation.  Alternatively, provide support for populating the created data object using non-default clipboard formats by calling method <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a> and specifying the format in the <b>FORMATETC</b> structure passed in parameter <i>pFormatetc</i>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This must be IID_IDataObject.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is typically called when implementing method <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a>. When an interface pointer of interface ID  IID_IDataObject is requested (using parameter <i>riid</i>), the implementer can return the interface pointer on the object created with <b>SHCreateDataObject</b> in response.

This function supports the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_SHELLIDLIST</a> (also known as HIDA) clipboard format and also has generic support for arbitrary clipboard formats through <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a>. For more information on clipboard formats, see Shell Clipboard Formats.

The new data object is intended to be used in operations such as drag-and-drop, in which the data is stored in the clipboard with a given format.

We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/4949c701-a375-450a-89a3-3fd146557d11">CIDLData_CreateFromIDArray</a>
 

 

