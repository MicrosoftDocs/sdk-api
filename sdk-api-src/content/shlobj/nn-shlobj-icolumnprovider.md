---
UID: NN:shlobj.IColumnProvider
title: IColumnProvider
author: windows-sdk-content
description: Exposes methods that enable the addition of custom columns in the Windows Explorer Details view.
old-location: shell\IColumnProvider.htm
old-project: shell
ms.assetid: 06993217-2867-43f2-aa76-04b500bf8c17
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IColumnProvider, IColumnProvider interface [Windows Shell], IColumnProvider interface [Windows Shell],described, _win32_IColumnProvider, shell.IColumnProvider, shlobj/IColumnProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IColumnProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IColumnProvider interface


## -description


Exposes methods that enable the addition of custom columns in the Windows Explorer Details view.
            
            
<div class="alert"><b>Note</b>  Support for <b>IColumnProvider</b> has been removed as of Windows Vista. The Windows property system is used in its place. See <a href="https://msdn.microsoft.com/c2094bbe-a4ca-4f30-b16e-14dced2912bc">Windows Property System</a> for conceptual materials that explain the use of the new system.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IColumnProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IColumnProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87196252-3835-4828-ad0a-0edcafb286b7">GetColumnInfo</a>
</td>
<td align="left" width="63%">
Requests information about a column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88e76f03-acc3-46b1-ad03-d2343f4f3dac">GetItemData</a>
</td>
<td align="left" width="63%">
Requests column data for a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4975042d-549e-4032-9f42-468dc7e3c20e">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IColumnProvider</b> interface.

</td>
</tr>
</table> 


## -remarks



The Windows Explorer Details view typically displays several standard columns. Each column lists information, such as the file size or type, for each file in the current folder. There can also be a number of columns that the user can choose to display. When the user right-clicks one of the column headers, a list of the available columns is displayed in a dialog box. By creating a column provider object that exports the <b>IColumnProvider</b> interface, you can add custom columns to that dialog box for display by Windows Explorer. For example, a collection of files that contain music could use a column provider to display columns listing the artist and piece contained by each file.

A column provider is a global object that is called every time Windows Explorer displays the Details view. Windows Explorer queries all registered column providers for their column characteristics. If the user has selected one of the column provider's columns, Windows Explorer queries the column provider for the associated data for each file in the folder. It then displays all the selected columns.

Typically, column providers are used to display one or more custom columns for a particular <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">file type</a>. When a column provider receives a request for data, it provides it if the file is a member of its supported type. Otherwise, it ignores the request by returning S_FALSE.

Columns are identified by an <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that contains an <b>fmtid</b>/<b>pid</b> pair. If possible, use existing <b>fmtid</b>s and <b>pid</b>s. If a folder contains files of more than one file type, the data from different types can be merged into the same column. For instance, the Author <b>pid</b> from the summary information property set can be used for a wide variety of purposes. If you use a custom <b>SHCOLUMNID</b> structure, the column will display data only for those files that are members of the supported type. If the folder contains other files, their entries will be blank.

Implement an object that exports this interface when you want to have one or more custom columns displayed in the Windows Explorer Details view. Windows Explorer calls the interface methods to request the information it needs to display the column. The procedure used by Windows Explorer is as follows:
		
        		

<ol>
<li>Call <a href="https://msdn.microsoft.com/4975042d-549e-4032-9f42-468dc7e3c20e">IColumnProvider::Initialize</a> to specify the folder to display.</li>
<li>Call <a href="https://msdn.microsoft.com/87196252-3835-4828-ad0a-0edcafb286b7">IColumnProvider::GetColumnInfo</a> to retrieve the column's characteristics.</li>
<li>If the column has been selected by the user, call <a href="https://msdn.microsoft.com/88e76f03-acc3-46b1-ad03-d2343f4f3dac">IColumnProvider::GetItemData</a> for each file in the folder to retrieve the data that belongs in the file's column entry.</li>
</ol>
In addition to normal Component Object Model (COM) registration, the column provider object must also be registered with Windows Explorer. To do so, add a subkey named with the string form of the object's GUID to this key.
		
        		<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>Folder</b>
      <b>shellex</b>
         <b>ColumnHandlers</b></pre>


This interface is called by Windows Explorer. It is not typically used by applications.



