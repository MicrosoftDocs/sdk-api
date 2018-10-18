---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetTypeLabel
title: ISyncMgrHandlerInfo::GetTypeLabel
author: windows-sdk-content
description: Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string.
old-location: shell\ISyncMgrHandlerInfo_GetTypeLabel.htm
tech.root: shell
ms.assetid: b1a30aad-bd8e-4375-a914-3010b86d83d9
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetTypeLabel, GetTypeLabel method [Windows Shell], GetTypeLabel method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetTypeLabel method, ISyncMgrHandlerInfo.GetTypeLabel, ISyncMgrHandlerInfo::GetTypeLabel, _shell_ISyncMgrHandlerInfo_GetTypeLabel, shell.ISyncMgrHandlerInfo_GetTypeLabel, syncmgr/ISyncMgrHandlerInfo::GetTypeLabel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISyncMgrHandlerInfo.GetTypeLabel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The label value is displayed as the System.Sync.HandlerTypeLabel (PKEY_Sync_HandlerTypeLabel) property in the folder UI. Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.

The handler is responsible for allocating the string buffer pointed to by <i>ppszTypeLabel</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### Examples



The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetTypeLabel(__out LPWSTR *ppszTypeLabel)
{
    LPWSTR pszTypeLabel = NULL;

    HRESULT hr = LoadStringAlloc(g_hmodThisDll, 
                                 IDS_HANDLER_TYPE_LABEL,
                                 &amp;pszTypeLabel);
    if (SUCCEEDED(hr))
    {
        // Duplicate for the caller.
        hr = SHCoAllocString(pszTypeLabel, ppszTypeLabel);
        LocalFree(pszTypeLabel);
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


