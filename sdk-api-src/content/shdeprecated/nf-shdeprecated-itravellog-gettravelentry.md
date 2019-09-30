---
UID: NF:shdeprecated.ITravelLog.GetTravelEntry
title: ITravelLog::GetTravelEntry (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Gets a travel entry in the travel log relative to the position of the current entry.
old-location: shell\ITravelLog_GetTravelEntry.htm
tech.root: shell
ms.assetid: 8db8aa9a-91c2-49fb-bbef-c7e19de09efe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTravelEntry, GetTravelEntry method [Windows Shell], GetTravelEntry method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],GetTravelEntry method, ITravelLog.GetTravelEntry, ITravelLog::GetTravelEntry, shdeprecated/ITravelLog::GetTravelEntry, shell.ITravelLog_GetTravelEntry, zone_ITravelLog_GetTravelEntry
ms.topic: method
f1_keywords: 
 - "shdeprecated/ITravelLog.GetTravelEntry"
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
 - ITravelLog.GetTravelEntry
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# ITravelLog::GetTravelEntry


## -description


Deprecated. Gets a travel entry in the travel log relative to the position of the current entry.


## -parameters




### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


### -param iOffset [in]

Type: <b>int</b>

The number of travel entries forward (a positive value) or backward (a negative value) to move in the travel log.


### -param ppte [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-itravelentry">ITravelEntry</a>**</b>

The address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-itravelentry">ITravelEntry</a> interface representing the travel entry at the offset specified in <i>iOffset</i>. This value is only valid if the method returns successfully.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>ITravelLog::GetTravelEntry</b> is often used to discover whether the <b>Back</b> and <b>Forward</b> buttons should be enabled in the browser window.



