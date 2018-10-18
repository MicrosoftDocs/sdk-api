---
UID: NF:shdeprecated.ITravelLog.UpdateExternal
title: ITravelLog::UpdateExternal
author: windows-sdk-content
description: Deprecated. Updates an entry that originated out of the current procedure through IHlinkFrame.
old-location: shell\ITravelLog_UpdateExternal.htm
tech.root: shell
ms.assetid: 2fda446d-8652-455b-9233-aa02f2a85e7f
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ITravelLog interface [Windows Shell],UpdateExternal method, ITravelLog.UpdateExternal, ITravelLog::UpdateExternal, UpdateExternal, UpdateExternal method [Windows Shell], UpdateExternal method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::UpdateExternal, shell.ITravelLog_UpdateExternal, zone_ITravelLog_UpdateExternal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - ITravelLog.UpdateExternal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# ITravelLog::UpdateExternal


## -description


Deprecated. Updates an entry that originated out of the current procedure through <a href="_inet_IHlinkFrame_Interface_cpp">IHlinkFrame</a>.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param punkHLBrowseContext [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of an <a href="_inet_IHlinkBrowseContext_Interface_cpp">IHlinkBrowseContext</a> retrieved through <a href="_inet_IHlinkFrame_Interface_inet_IHlinkFrame_GetBrowseContext_Method_cpp">IHlinkFrame::GetBrowseContext</a>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



