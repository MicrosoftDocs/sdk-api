---
UID: NN:shobjidl_core.IObjectWithBackReferences
title: IObjectWithBackReferences (shobjidl_core.h)
description: Provides a method for interacting with back references held by an object.
helpviewer_keywords: ["IObjectWithBackReferences","IObjectWithBackReferences interface [Windows Shell]","IObjectWithBackReferences interface [Windows Shell]","described","_shell_IObjectWithBackReferences","shell.IObjectWithBackReferences","shobjidl_core/IObjectWithBackReferences"]
old-location: shell\IObjectWithBackReferences.htm
tech.root: shell
ms.assetid: 9ce0edc6-c2b1-4222-a12b-daf94efcb233
ms.date: 12/05/2018
ms.keywords: IObjectWithBackReferences, IObjectWithBackReferences interface [Windows Shell], IObjectWithBackReferences interface [Windows Shell],described, _shell_IObjectWithBackReferences, shell.IObjectWithBackReferences, shobjidl_core/IObjectWithBackReferences
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectWithBackReferences
 - shobjidl_core/IObjectWithBackReferences
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
 - IObjectWithBackReferences
---

# IObjectWithBackReferences interface


## -description

Provides a method for interacting with back references held by an object.

## -inheritance

The <b>IObjectWithBackReferences</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithBackReferences</b> also has these types of members:

## -remarks

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
When an object contains forward references to child objects that have back references to the parent object, circular references can occur. To break this circle, the parent object needs to keep track of back references from child objects.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface should be implemented by Shell data source objects (objects that implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>) that hold references to other objects in a way that might result in reference cycles. For example, an object that maintains references to other data source objects that are cached as the result of binding operations should implement this interface.

This interface was available in Windows Vista with Service Pack 1 (SP1), but it was not declared in a public header until Windows 7. For use in Windows Vista with SP1, the following Interface Definition Language (IDL) fragment describes this interface, including its IID.
                
                


```cpp
object,
    uuid(321a6a6a-d61f-4bf3-97ae-14be2986bb36),
    pointer_default(unique)
]
interface IObjectWithBackReferences : IUnknown
{
    HRESULT RemoveBackReferences();
}

```


The following C++ fragment can be used to enable access to this interface.
                


```cpp
struct 
    __declspec(uuid("321a6a6a-d61f-4bf3-97ae-14be2986bb36")) 
    __declspec(novtable)
IObjectWithBackReferences : public IUnknown
{
    public:
        virtual HRESULT __stdcall RemoveBackReferences() = 0;
};

```
