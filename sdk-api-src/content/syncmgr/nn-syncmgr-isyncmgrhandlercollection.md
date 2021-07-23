---
UID: NN:syncmgr.ISyncMgrHandlerCollection
title: ISyncMgrHandlerCollection (syncmgr.h)
description: Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers.
helpviewer_keywords: ["ISyncMgrHandlerCollection","ISyncMgrHandlerCollection interface [Windows Shell]","ISyncMgrHandlerCollection interface [Windows Shell]","described","_shell_ISyncMgrHandlerCollection","shell.ISyncMgrHandlerCollection","syncmgr/ISyncMgrHandlerCollection"]
old-location: shell\ISyncMgrHandlerCollection.htm
tech.root: shell
ms.assetid: 24514602-42c0-41ef-be33-fce03e7f091a
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerCollection, ISyncMgrHandlerCollection interface [Windows Shell], ISyncMgrHandlerCollection interface [Windows Shell],described, _shell_ISyncMgrHandlerCollection, shell.ISyncMgrHandlerCollection, syncmgr/ISyncMgrHandlerCollection
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - ISyncMgrHandlerCollection
 - syncmgr/ISyncMgrHandlerCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandlerCollection
---

# ISyncMgrHandlerCollection interface


## -description

Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers.

## -inheritance

The <b>ISyncMgrHandlerCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandlerCollection</b> also has these types of members:

## -remarks

The author of a sync handler implements this interface to support multiple devices or computers and sync their details independently. Sync Center uses the handler collection to request instantiation of individual sync handlers. <b>ISyncMgrHandlerCollection</b> also allows a sync handler author to add handlers dynamically to Sync Center as opposed to registering each one individually in the registry.

The following example shows an outline implementation of this interface.


```cpp
class CMyHandlerCollection : public ISyncMgrHandlerCollection
{
public:
    // IUnknown
    // ISyncMgrHandlerCollection
    IFACEMETHODIMP GetHandlerEnumerator(__out IEnumString **ppenum);
    IFACEMETHODIMP BindToHandler(
        __in LPCWSTR    pszHandlerID,
        __in REFIID     riid,
        __out void    **ppv);
};

STDMETHODIMP CMyHandlerCollection::GetHandlerEnumerator(
    __out IEnumString **ppenum)
{
    // IDs are retrieved from a data source such as the registry.
    // IDs could be retrieved either by this collection class 
    // or the factory method.
    return CEnumMyHandlerIDs_Create(ppenum);
}

STDMETHODIMP CMyHandlerCollection::BindToHandler(
    __in LPCWSTR    pszHandlerID,
    __in REFIID     riid,
    __out void    **ppv)
{
    // Map the pszHandlerID to the handler to create. This could be done
    // by the factory method or by some other method.
    return CMyHandler_Create(pszHandlerID, riid, ppv);
}

```
