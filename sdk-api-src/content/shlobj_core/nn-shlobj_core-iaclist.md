---
UID: NN:shlobj_core.IACList
title: IACList (shlobj_core.h)
description: Exposes a method that improves the efficiency of autocompletion when the candidate strings are organized in a hierarchy.
helpviewer_keywords: ["IACList","IACList interface [Windows Shell]","IACList interface [Windows Shell]","described","_win32_IACList","shell.IACList","shlobj_core/IACList"]
old-location: shell\IACList.htm
tech.root: shell
ms.assetid: 66513683-38ca-4b19-88d5-d14bf7ae73eb
ms.date: 12/05/2018
ms.keywords: IACList, IACList interface [Windows Shell], IACList interface [Windows Shell],described, _win32_IACList, shell.IACList, shlobj_core/IACList
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IACList
 - shlobj_core/IACList
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
 - IACList
---

# IACList interface


## -description

Exposes a method that improves the efficiency of <a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">autocompletion</a> when the candidate strings are organized in a hierarchy.

## -inheritance

The <b>IACList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IACList</b> also has these types of members:

## -remarks

Autocompletion typically requires the following three components:
		
        		

<ul>
<li>The autocompletion client. This client is a window, such as a dialog box, that hosts the edit control.</li>
<li>The autocompletion object (CLSID_AutoComplete). This object is provided by the system, and handles the user interface, parsing, and background thread management.</li>
<li>The autocompletion list object. This object is responsible for providing lists of candidate strings to the autocompletion object.</li>
</ul>
A simple autocompletion list object needs only to export <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> in addition to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. When the user enters characters in the edit box, the autocompletion object calls the list object's <b>IEnumString</b> interface to enumerate the list of strings that can be used to complete the partial string. The list object maintains a namespace and decides which of those strings are relevant.

The simplest approach a list object takes is to return every string in its namespace every time the autocompletion object makes a request. For a discussion of how to implement this type of list object, see <a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">IAutoComplete</a>. However, this approach is practical only if the namespace is relatively small. When large numbers of strings are involved, the list object must restrict itself to a small subset of the namespace.

The <b>IACList</b> interface is exported by autocompletion list objects to help them choose a sensible subset of strings from a hierarchically organized namespace. With a large namespace, this procedure substantially increases the efficiency of autocompletion. The basic procedure is as follows:

				

<ol>
<li>The autocomplete object calls the list object's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface. The list object returns the names of the top-level items in the hierarchy. For example, if the namespace consists of every file and folder on the C: drive, the list object returns the fully qualified paths of the folders and files contained in the C:\ directory.</li>
<li>The user continues to type until he or she enters a delimiter. The '\' and '/' characters are recognized as delimiters by the autocompletion object.</li>
<li>The autocompletion object calls the list object's <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iaclist-expand">IACList::Expand</a> method and passes it the current partial string.</li>
<li>The autocomplete object calls the list object's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface again to request a new list of strings. If the partial string matches one of the top-level items in the namespace, the list object returns the names of the items that fall immediately under the selected item. For instance, if the user has entered "C:\Program Files\", the list object returns the names of the files and folders contained in that directory. If the name passed to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iaclist-expand">IACList::Expand</a> does not match any top-level item, the list object can simply stop returning strings until the autocomplete object calls <b>IACList::Expand</b> with a string that is in the list object's namespace.</li>
<li>The process continues until the user selects a string, typically by pressing the <b>ENTER</b> key.</li>
</ol>
