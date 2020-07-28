---
UID: NN:wmiutils.IWbemPath
title: IWbemPath (wmiutils.h)
description: The IWbemPath interface is the primary interface for the object path parser and makes parsing a path available to programs in a standard way. This interface is the main interface for setting and retrieving path information.
helpviewer_keywords: ["IWbemPath","IWbemPath interface [Windows Management Instrumentation]","IWbemPath interface [Windows Management Instrumentation]","described","WbemDefPath","_hmm_iwbempath","wmi.iwbempath","wmiutils/IWbemPath"]
old-location: wmi\iwbempath.htm
tech.root: wmi
ms.assetid: 71b2597b-d82a-439d-b0b7-af76aefea6a2
ms.date: 12/05/2018
ms.keywords: IWbemPath, IWbemPath interface [Windows Management Instrumentation], IWbemPath interface [Windows Management Instrumentation],described, WbemDefPath, _hmm_iwbempath, wmi.iwbempath, wmiutils/IWbemPath
f1_keywords:
- wmiutils/IWbemPath
dev_langs:
- c++
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmiutils.dll
api_name:
- IWbemPath
- IWbemPath.SetScopeFromText
- WbemDefPath
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemPath interface


## -description


The 
<b>IWbemPath</b> interface is the primary interface for the object path parser and makes parsing a path available to programs in a standard way. This interface is the main interface for setting and retrieving path information.

The following table lists the methods for 
<b>IWbemPath</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemPath</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemPath</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemPath</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-createclasspart">CreateClassPart</a>
</td>
<td align="left" width="63%">
Initializes the class/key portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-deleteclasspart">DeleteClassPart</a>
</td>
<td align="left" width="63%">
Deletes the class portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getclassname">GetClassName</a>
</td>
<td align="left" width="63%">
Retrieves the class name from the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Returns details about a path that has been placed into a parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getkeylist">GetKeyList</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a> pointer so that the individual key may be accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getnamespaceat">GetNamespaceAt</a>
</td>
<td align="left" width="63%">
Retrieves a namespace based upon its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getnamespacecount">GetNamespaceCount</a>
</td>
<td align="left" width="63%">
Returns the number of namespaces in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getscope">GetScope</a>
</td>
<td align="left" width="63%">
Retrieves a scope based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getscopeastext">GetScopeAsText</a>
</td>
<td align="left" width="63%">
Retrieves a scope in text format based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getscopecount">GetScopeCount</a>
</td>
<td align="left" width="63%">
Returns the number of scopes in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-getserver">GetServer</a>
</td>
<td align="left" width="63%">
Returns the server portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-gettext">GetText</a>
</td>
<td align="left" width="63%">
Returns a textual representation of a path that has previously been placed into a parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-islocal">IsLocal</a>
</td>
<td align="left" width="63%">
Tests if the computer name passed in matches the computer name in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-isrelative">IsRelative</a>
</td>
<td align="left" width="63%">
Tests if the path is relative to a particular computer and namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-isrelativeorchild">IsRelativeOrChild</a>
</td>
<td align="left" width="63%">
Tests if the path is relative to or a child of a particular computer and namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-issameclassname">IsSameClassName</a>
</td>
<td align="left" width="63%">
Tests whether the class name passed in matches the one in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-removeallnamespaces">RemoveAllNamespaces</a>
</td>
<td align="left" width="63%">
Removes the namespace portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-removeallscopes">RemoveAllScopes</a>
</td>
<td align="left" width="63%">
Removes all scopes from the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-removenamespaceat">RemoveNamespaceAt</a>
</td>
<td align="left" width="63%">
Removes a namespace at a particular index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-removescope">RemoveScope</a>
</td>
<td align="left" width="63%">
Removes a scope based on the index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-setclassname">SetClassName</a>
</td>
<td align="left" width="63%">
Sets the class name portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-setnamespaceat">SetNamespaceAt</a>
</td>
<td align="left" width="63%">
Sets a namespace's value in the path based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-setscope">SetScope</a>
</td>
<td align="left" width="63%">
Sets a scope in the path based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetScopeFromText</b></td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-setserver">SetServer</a>
</td>
<td align="left" width="63%">
Sets the server portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmiutils/nf-wmiutils-iwbempath-settext">SetText</a>
</td>
<td align="left" width="63%">
Parses a path so that information on the path can be returned by the path parser.

</td>
</tr>
</table> 

