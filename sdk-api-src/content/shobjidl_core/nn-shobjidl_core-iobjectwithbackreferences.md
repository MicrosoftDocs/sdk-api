---
UID: NN:shobjidl_core.IObjectWithBackReferences
title: IObjectWithBackReferences
author: windows-sdk-content
description: Provides a method for interacting with back references held by an object.
old-location: shell\IObjectWithBackReferences.htm
tech.root: shell
ms.assetid: 9ce0edc6-c2b1-4222-a12b-daf94efcb233
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IObjectWithBackReferences, IObjectWithBackReferences interface [Windows Shell], IObjectWithBackReferences interface [Windows Shell],described, _shell_IObjectWithBackReferences, shell.IObjectWithBackReferences, shobjidl_core/IObjectWithBackReferences
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithBackReferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithBackReferences interface


## -description


Provides a method for interacting with back references held by an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithBackReferences</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithBackReferences</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithBackReferences</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/642fe793-974f-48e5-90a2-de6ba7a5b033">RemoveBackReferences</a>
</td>
<td align="left" width="63%">
Removes all back references held by an object.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
When an object contains forward references to child objects that have back references to the parent object, circular references can occur. To break this circle, the parent object needs to keep track of back references from child objects.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface should be implemented by Shell data source objects (objects that implement <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>) that hold references to other objects in a way that might result in reference cycles. For example, an object that maintains references to other data source objects that are cached as the result of binding operations should implement this interface.

This interface was available in Windows Vista with Service Pack 1 (SP1), but it was not declared in a public header until Windows 7. For use in Windows Vista with SP1, the following Interface Definition Language (IDL) fragment describes this interface, including its IID.
                
                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>object,
    uuid(321a6a6a-d61f-4bf3-97ae-14be2986bb36),
    pointer_default(unique)
]
interface IObjectWithBackReferences : IUnknown
{
    HRESULT RemoveBackReferences();
}
</pre>
</td>
</tr>
</table></span></div>
The following C++ fragment can be used to enable access to this interface.
                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>struct 
    __declspec(uuid("321a6a6a-d61f-4bf3-97ae-14be2986bb36")) 
    __declspec(novtable)
IObjectWithBackReferences : public IUnknown
{
    public:
        virtual HRESULT __stdcall RemoveBackReferences() = 0;
};
</pre>
</td>
</tr>
</table></span></div>


