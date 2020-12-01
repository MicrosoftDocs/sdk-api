---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetTypeLabel
title: ISyncMgrHandlerInfo::GetTypeLabel (syncmgr.h)
description: Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string.
helpviewer_keywords: ["GetTypeLabel","GetTypeLabel method [Windows Shell]","GetTypeLabel method [Windows Shell]","ISyncMgrHandlerInfo interface","ISyncMgrHandlerInfo interface [Windows Shell]","GetTypeLabel method","ISyncMgrHandlerInfo.GetTypeLabel","ISyncMgrHandlerInfo::GetTypeLabel","_shell_ISyncMgrHandlerInfo_GetTypeLabel","shell.ISyncMgrHandlerInfo_GetTypeLabel","syncmgr/ISyncMgrHandlerInfo::GetTypeLabel"]
old-location: shell\ISyncMgrHandlerInfo_GetTypeLabel.htm
tech.root: shell
ms.assetid: b1a30aad-bd8e-4375-a914-3010b86d83d9
ms.date: 12/05/2018
ms.keywords: GetTypeLabel, GetTypeLabel method [Windows Shell], GetTypeLabel method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetTypeLabel method, ISyncMgrHandlerInfo.GetTypeLabel, ISyncMgrHandlerInfo::GetTypeLabel, _shell_ISyncMgrHandlerInfo_GetTypeLabel, shell.ISyncMgrHandlerInfo_GetTypeLabel, syncmgr/ISyncMgrHandlerInfo::GetTypeLabel
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
 - ISyncMgrHandlerInfo::GetTypeLabel
 - syncmgr/ISyncMgrHandlerInfo::GetTypeLabel
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
 - ISyncMgrHandlerInfo.GetTypeLabel
---

# ISyncMgrHandlerInfo::GetTypeLabel


## -description

Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string.

## -parameters

### -param ppszTypeLabel [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the label string.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>ppszTypeLabel</i> contains an empty string.

## -remarks

The label value is displayed as the System.Sync.HandlerTypeLabel (PKEY_Sync_HandlerTypeLabel) property in the folder UI. Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.

The handler is responsible for allocating the string buffer pointed to by <i>ppszTypeLabel</i> through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetTypeLabel(__out LPWSTR *ppszTypeLabel)
{
    LPWSTR pszTypeLabel = NULL;

    HRESULT hr = LoadStringAlloc(g_hmodThisDll, 
                                 IDS_HANDLER_TYPE_LABEL,
                                 &pszTypeLabel);
    if (SUCCEEDED(hr))
    {
        // Duplicate for the caller.
        hr = SHCoAllocString(pszTypeLabel, ppszTypeLabel);
        LocalFree(pszTypeLabel);
    }

    return hr;
}

```