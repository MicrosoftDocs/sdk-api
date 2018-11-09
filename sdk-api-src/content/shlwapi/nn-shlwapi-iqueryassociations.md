---
UID: NN:shlwapi.IQueryAssociations
title: IQueryAssociations
author: windows-sdk-content
description: Exposes methods that simplify the process of retrieving information stored in the registry in association with defining a file type or protocol and associating it with an application.
old-location: shell\IQueryAssociations.htm
tech.root: shell
ms.assetid: 8edb99d3-5860-4d78-a750-1df34cdfc313
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IQueryAssociations, IQueryAssociations interface [Windows Shell], IQueryAssociations interface [Windows Shell],described, _win32_IQueryAssociations, shell.IQueryAssociations, shlwapi/IQueryAssociations
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryAssociations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryAssociations interface


## -description


Exposes methods that simplify the process of retrieving information stored in the registry in association with defining a file type or protocol and associating it with an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryAssociations</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueryAssociations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryAssociations</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">GetData</a>
</td>
<td align="left" width="63%">
Searches for and retrieves file or protocol association-related binary data from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad1e920c-4225-4f0b-b182-60028c9224c6">GetEnum</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f380a9e-fda0-46be-88a1-fd73b0a4b7b7">GetKey</a>
</td>
<td align="left" width="63%">
Searches for and retrieves a file or protocol association-related key from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">GetString</a>
</td>
<td align="left" width="63%">
Searches for and retrieves a file or protocol association-related string from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb1bcfc1-dbaa-48f8-8547-408f6560753e">Init</a>
</td>
<td align="left" width="63%">
Initializes the <b>IQueryAssociations</b> interface and sets the root key to the appropriate ProgID.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is exposed by the Shell or by namespace extensions to simplify handling file and protocol associations. You should not implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface if you need information from the registry related to file or protocol associations. For example, you can use this interface to retrieve information associated with a file name extension such as the command string of one of its verbs.

A complete registry path or HKEY value is not required. Instead, you can retrieve information based on criteria such as the file name extension or executable name. For a discussion of file associations, see <a href="https://msdn.microsoft.com/055648cd-46ce-4e61-80b2-bcf1d1823e20">File Types</a>.

You can also retrieve an application's name using this interface. Use method <a href="https://msdn.microsoft.com/72463664-783b-4375-a6ba-43633a82ec7e">IQueryAssociations::GetString</a>. Set the <i>str</i> parameter to <a href="https://msdn.microsoft.com/b5fd3d25-3630-4dd8-acd2-d2e4ed571604">ASSOCSTR_FRIENDLYAPPNAME</a>.

To use this interface, you must first retrieve a pointer to it. Typically, you retrieve an <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> pointer by calling a Shell object's <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> method. You can also retrieve an interface pointer by calling <a href="https://msdn.microsoft.com/33099e0e-73e3-4047-804f-765a59e42e3f">AssocCreate</a> (set <i>clsid</i> to CLSID_QueryAssociations). Initialize the interface with <a href="https://msdn.microsoft.com/cb1bcfc1-dbaa-48f8-8547-408f6560753e">IQueryAssociations::Init</a>. This method sets the root key that will be used when you call any of the remaining three methods to retrieve information from the registry. They will look only below the root key. You must release the interface when you no longer need it.

The <b>IQueryAssociations</b> interface is useful if you need to repeatedly query the registry for information. Once the interface is initialized, the overhead of calling the various methods is relatively small. There are also several related functions, listed in the See Also section, that allow you to retrieve the same information from the registry with a single function call. While they are simpler to use, they cause the overhead of creating and initializing <b>IQueryAssociations</b> each time they are called. Because of this, they are best suited for single use.




## -see-also




<a href="https://msdn.microsoft.com/9eaeb885-0428-48c3-82a7-5dc21d5015ce">AssocQueryKey</a>



<a href="https://msdn.microsoft.com/026b841d-b831-475e-a788-2c79801e20b8">AssocQueryString</a>



<a href="https://msdn.microsoft.com/6816f7fe-9a70-4c5f-bd45-d1ca96d4ebd0">AssocQueryStringByKey</a>
 

 

