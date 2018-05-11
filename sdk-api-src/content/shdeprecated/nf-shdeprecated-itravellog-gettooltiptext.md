---
UID: NF:shdeprecated.ITravelLog.GetToolTipText
title: ITravelLog::GetToolTipText
author: windows-driver-content
description: Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.
old-location: shell\ITravelLog_GetToolTipText.htm
old-project: shell
ms.assetid: a085fe2e-9658-448c-b659-4ef08896ec77
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetToolTipText, GetToolTipText method [Windows Shell], GetToolTipText method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],GetToolTipText method, ITravelLog.GetToolTipText, ITravelLog::GetToolTipText, shdeprecated/ITravelLog::GetToolTipText, shell.ITravelLog_GetToolTipText, zone_ITravelLog_GetToolTipText
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
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	ITravelLog.GetToolTipText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# ITravelLog::GetToolTipText


## -description


Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param iOffset [in]

Type: <b>int</b>

The number of travel entries forward (a positive value) or backward (a negative value) to move in the travel log to arrive at the travel entry from which text should be retrieved.


### -param idsTemplate [in]

Type: <b>int</b>

Not used.


### -param pwzText [out]

Type: <b>LPWSTR</b>

A pointer to a buffer that receives the Unicode tooltip text string.


### -param cchText [in]

Type: <b>DWORD</b>


          The number of characters in the buffer pointed to by <i>pwzText</i>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



