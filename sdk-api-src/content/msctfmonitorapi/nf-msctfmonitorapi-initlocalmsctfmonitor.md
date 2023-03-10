---
UID: NF:msctfmonitorapi.InitLocalMsCtfMonitor
title: InitLocalMsCtfMonitor function (msctfmonitorapi.h)
description: The InitLocalMsCtfMonitor function initializes TextServicesFramework on the current desktop and prepares the floating language bar, if necessary. This function must be called on the app's desktop.
helpviewer_keywords: ["ILMCM_CHECKLAYOUTANDTIPENABLED","ILMCM_LANGUAGEBAROFF","InitLocalMsCtfMonitor","InitLocalMsCtfMonitor function [Text Services Framework]","msctfmonitorapi/InitLocalMsCtfMonitor","tsf.InitLocalMsCtfMonitor"]
old-location: tsf\InitLocalMsCtfMonitor.htm
tech.root: TSF
ms.assetid: d382afea-e30a-4aeb-a357-551fee6229ae
ms.date: 12/05/2018
ms.keywords: ILMCM_CHECKLAYOUTANDTIPENABLED, ILMCM_LANGUAGEBAROFF, InitLocalMsCtfMonitor, InitLocalMsCtfMonitor function [Text Services Framework], msctfmonitorapi/InitLocalMsCtfMonitor, tsf.InitLocalMsCtfMonitor
req.header: msctfmonitorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MsCtfMonitor.lib
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitLocalMsCtfMonitor
 - msctfmonitorapi/InitLocalMsCtfMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - InitLocalMsCtfMonitor
---

# InitLocalMsCtfMonitor function


## -description

The <b>InitLocalMsCtfMonitor</b> function initializes TextServicesFramework on the current desktop and prepares the floating language bar, if necessary. This function must be called on the app's desktop.

## -parameters

### -param dwFlags [in]

This is a combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILMCM_CHECKLAYOUTANDTIPENABLED"></a><a id="ilmcm_checklayoutandtipenabled"></a><dl>
<dt><b>ILMCM_CHECKLAYOUTANDTIPENABLED</b></dt>
</dl>
</td>
<td width="60%">
<b>InitLocalMsCtfMonitor</b> forcefully checks the available keyboard layout or text service. If there is no secondary keyboard layout or text services, it does not initialize TextServicesFramework on the desktop.

</td>
</tr>
<tr>
<td width="40%"><a id="ILMCM_LANGUAGEBAROFF"></a><a id="ilmcm_languagebaroff"></a><dl>
<dt><b>ILMCM_LANGUAGEBAROFF</b></dt>
</dl>
</td>
<td width="60%">
<b>Starting with Windows 8:</b> A local language bar is not started for the current desktop.

</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The function was successful.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

If this function was successful, <a href="/windows/desktop/api/msctfmonitorapi/nf-msctfmonitorapi-uninitlocalmsctfmonitor">UninitLocalMsCtfMonitor</a> needs to be called before the caller thread is terminated or the desktop is switched.