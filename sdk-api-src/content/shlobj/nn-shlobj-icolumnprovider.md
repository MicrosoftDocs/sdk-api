---
UID: NN:shlobj.IColumnProvider
title: IColumnProvider (shlobj.h)
description: Exposes methods that enable the addition of custom columns in the Windows Explorer Details view.
helpviewer_keywords: ["IColumnProvider","IColumnProvider interface [Windows Shell]","IColumnProvider interface [Windows Shell]","described","_win32_IColumnProvider","shell.IColumnProvider","shlobj/IColumnProvider"]
old-location: shell\IColumnProvider.htm
tech.root: shell
ms.assetid: 06993217-2867-43f2-aa76-04b500bf8c17
ms.date: 12/05/2018
ms.keywords: IColumnProvider, IColumnProvider interface [Windows Shell], IColumnProvider interface [Windows Shell],described, _win32_IColumnProvider, shell.IColumnProvider, shlobj/IColumnProvider
req.header: shlobj.h
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IColumnProvider
 - shlobj/IColumnProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IColumnProvider
---

# IColumnProvider interface


## -description

Exposes methods that enable the addition of custom columns in the Windows Explorer Details view.
            
            
<div class="alert"><b>Note</b>  Support for <b>IColumnProvider</b> has been removed as of Windows Vista. The Windows property system is used in its place. See <a href="/windows/desktop/properties/windows-properties-system">Windows Property System</a> for conceptual materials that explain the use of the new system.</div><div> </div>

## -inheritance

The <b>IColumnProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IColumnProvider</b> also has these types of members:

## -remarks

The Windows Explorer Details view typically displays several standard columns. Each column lists information, such as the file size or type, for each file in the current folder. There can also be a number of columns that the user can choose to display. When the user right-clicks one of the column headers, a list of the available columns is displayed in a dialog box. By creating a column provider object that exports the <b>IColumnProvider</b> interface, you can add custom columns to that dialog box for display by Windows Explorer. For example, a collection of files that contain music could use a column provider to display columns listing the artist and piece contained by each file.

A column provider is a global object that is called every time Windows Explorer displays the Details view. Windows Explorer queries all registered column providers for their column characteristics. If the user has selected one of the column provider's columns, Windows Explorer queries the column provider for the associated data for each file in the folder. It then displays all the selected columns.

Typically, column providers are used to display one or more custom columns for a particular <a href="/windows/desktop/shell/fa-file-types">file type</a>. When a column provider receives a request for data, it provides it if the file is a member of its supported type. Otherwise, it ignores the request by returning S_FALSE.

Columns are identified by an <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure that contains an <b>fmtid</b>/<b>pid</b> pair. If possible, use existing <b>fmtid</b>s and <b>pid</b>s. If a folder contains files of more than one file type, the data from different types can be merged into the same column. For instance, the Author <b>pid</b> from the summary information property set can be used for a wide variety of purposes. If you use a custom <b>SHCOLUMNID</b> structure, the column will display data only for those files that are members of the supported type. If the folder contains other files, their entries will be blank.

Implement an object that exports this interface when you want to have one or more custom columns displayed in the Windows Explorer Details view. Windows Explorer calls the interface methods to request the information it needs to display the column. The procedure used by Windows Explorer is as follows:
		
        		

<ol>
<li>Call <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize">IColumnProvider::Initialize</a> to specify the folder to display.</li>
<li>Call <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo">IColumnProvider::GetColumnInfo</a> to retrieve the column's characteristics.</li>
<li>If the column has been selected by the user, call <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata">IColumnProvider::GetItemData</a> for each file in the folder to retrieve the data that belongs in the file's column entry.</li>
</ol>
In addition to normal Component Object Model (COM) registration, the column provider object must also be registered with Windows Explorer. To do so, add a subkey named with the string form of the object's GUID to this key.
		
        		<pre><b>HKEY_CLASSES_ROOT</b>
   <b>Folder</b>
      <b>shellex</b>
         <b>ColumnHandlers</b></pre>


This interface is called by Windows Explorer. It is not typically used by applications.
