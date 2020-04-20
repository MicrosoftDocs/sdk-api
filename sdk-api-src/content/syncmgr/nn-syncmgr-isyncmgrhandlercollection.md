---
UID: NN:syncmgr.ISyncMgrHandlerCollection
title: ISyncMgrHandlerCollection (syncmgr.h)
description: Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers.helpviewer_keywords: ["ISyncMgrHandlerCollection","ISyncMgrHandlerCollection interface [Windows Shell]","ISyncMgrHandlerCollection interface [Windows Shell]","described","_shell_ISyncMgrHandlerCollection","shell.ISyncMgrHandlerCollection","syncmgr/ISyncMgrHandlerCollection"]
old-location: shell\ISyncMgrHandlerCollection.htm
tech.root: shell
ms.assetid: 24514602-42c0-41ef-be33-fce03e7f091a
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerCollection, ISyncMgrHandlerCollection interface [Windows Shell], ISyncMgrHandlerCollection interface [Windows Shell],described, _shell_ISyncMgrHandlerCollection, shell.ISyncMgrHandlerCollection, syncmgr/ISyncMgrHandlerCollection
f1_keywords:
- syncmgr/ISyncMgrHandlerCollection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Syncmgr.h
api_name:
- ISyncMgrHandlerCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrHandlerCollection interface


## -description


Exposes methods that provide an enumerator of sync handler IDs and instantiate those sync handlers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrHandlerCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandlerCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrHandlerCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlercollection-bindtohandler">BindToHandler</a>
</td>
<td align="left" width="63%">
Instantiates a specified sync handler when called by Sync Center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlercollection-gethandlerenumerator">GetHandlerEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user.

</td>
</tr>
</table> 


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




