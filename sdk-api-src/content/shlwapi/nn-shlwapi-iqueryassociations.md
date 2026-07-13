---
UID: NN:shlwapi.IQueryAssociations
title: IQueryAssociations (shlwapi.h)
description: Exposes methods that simplify the process of retrieving information stored in the registry in association with defining a file type or protocol and associating it with an application.
helpviewer_keywords: ["IQueryAssociations","IQueryAssociations interface [Windows Shell]","IQueryAssociations interface [Windows Shell]","described","_win32_IQueryAssociations","shell.IQueryAssociations","shlwapi/IQueryAssociations"]
old-location: shell\IQueryAssociations.htm
tech.root: shell
ms.assetid: 8edb99d3-5860-4d78-a750-1df34cdfc313
ms.date: 12/05/2018
ms.keywords: IQueryAssociations, IQueryAssociations interface [Windows Shell], IQueryAssociations interface [Windows Shell],described, _win32_IQueryAssociations, shell.IQueryAssociations, shlwapi/IQueryAssociations
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
 - IQueryAssociations
 - shlwapi/IQueryAssociations
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
 - IQueryAssociations
---

# IQueryAssociations interface


## -description

Exposes methods that simplify the process of retrieving information stored in the registry in association with defining a file type or protocol and associating it with an application.

## -inheritance

The <b>IQueryAssociations</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryAssociations</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is exposed by the Shell or by namespace extensions to simplify handling file and protocol associations. You should not implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface if you need information from the registry related to file or protocol associations. For example, you can use this interface to retrieve information associated with a file name extension such as the command string of one of its verbs.

A complete registry path or HKEY value is not required. Instead, you can retrieve information based on criteria such as the file name extension or executable name. For a discussion of file associations, see <a href="/windows/desktop/shell/fa-file-types">File Types</a>.

You can also retrieve an application's name using this interface. Use method <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring">IQueryAssociations::GetString</a>. Set the <i>str</i> parameter to <a href="/windows/desktop/api/shlwapi/ne-shlwapi-assocstr">ASSOCSTR_FRIENDLYAPPNAME</a>.

To use this interface, you must first retrieve a pointer to it. Typically, you retrieve an <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> pointer by calling a Shell object's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method. You can also retrieve an interface pointer by calling <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate">AssocCreate</a> (set <i>clsid</i> to CLSID_QueryAssociations). Initialize the interface with <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-init">IQueryAssociations::Init</a>. This method sets the root key that will be used when you call any of the remaining three methods to retrieve information from the registry. They will look only below the root key. You must release the interface when you no longer need it.

The <b>IQueryAssociations</b> interface is useful if you need to repeatedly query the registry for information. Once the interface is initialized, the overhead of calling the various methods is relatively small. There are also several related functions, listed in the See Also section, that allow you to retrieve the same information from the registry with a single function call. While they are simpler to use, they cause the overhead of creating and initializing <b>IQueryAssociations</b> each time they are called. Because of this, they are best suited for single use.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya">AssocQueryKey</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa">AssocQueryString</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya">AssocQueryStringByKey</a>
