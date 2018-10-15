---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetType
title: ISyncMgrHandlerInfo::GetType
author: windows-sdk-content
description: Gets the handler type for Sync Center.
old-location: shell\ISyncMgrHandlerInfo_GetType.htm
tech.root: shell
ms.assetid: 466c5bd5-0166-4c0d-801d-a155f20140ce
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetType, GetType method [Windows Shell], GetType method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetType method, ISyncMgrHandlerInfo.GetType, ISyncMgrHandlerInfo::GetType, _shell_ISyncMgrHandlerInfo_GetType, shell.ISyncMgrHandlerInfo_GetType, syncmgr/ISyncMgrHandlerInfo::GetType
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
 - ISyncMgrHandlerInfo.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrHandlerInfo::GetType


## -description


Gets the handler type for Sync Center.


## -parameters




### -param pnType [out]

Type: <b><a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a>*</b>

When this method returns, points to a value from the <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a> enumeration that specifies the handler type. If the method fails, this parameter points to <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HT_UNSPECIFIED</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>pnType</i> is set to <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HT_UNSPECIFIED</a>.




## -remarks



Typically, this value does not change. However, Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetType(__out SYNCMGR_HANDLER_TYPE *pnType)
{
    *pnType = SYNCMGR_HT_DEVICE;
    return S_OK;

```




