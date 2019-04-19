---
UID: NF:wpcapi.IWPCWebSettings.GetSettings
title: IWPCWebSettings::GetSettings (wpcapi.h)
author: windows-sdk-content
description: Retrieves the web restrictions settings.
old-location: parcon\iwpcwebsettings_getsettings.htm
tech.root: parcon
ms.assetid: bf0c1a54-ac36-45f4-8005-1847dc00bf7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSettings, GetSettings method, GetSettings method,IWPCWebSettings interface, IWPCWebSettings interface,GetSettings method, IWPCWebSettings.GetSettings, IWPCWebSettings::GetSettings, WPCFLAG_WEB_SETTING_DOWNLOADSBLOCKED, WPCFLAG_WEB_SETTING_NOTBLOCKED, parcon.iwpcwebsettings_getsettings, wpcapi/IWPCWebSettings::GetSettings
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Wpcapi.h
api_name:
 - IWPCWebSettings.GetSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWPCWebSettings::GetSettings


## -description


Retrieves the web restrictions settings.


## -parameters




### -param pdwSettings [out]

The settings. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WEB_SETTING_NOTBLOCKED"></a><a id="wpcflag_web_setting_notblocked"></a><dl>
<dt><b>WPCFLAG_WEB_SETTING_NOTBLOCKED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
There are no restrictions.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WEB_SETTING_DOWNLOADSBLOCKED"></a><a id="wpcflag_web_setting_downloadsblocked"></a><dl>
<dt><b>WPCFLAG_WEB_SETTING_DOWNLOADSBLOCKED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Downloads are blocked.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/80629db8-0040-4545-a313-5cf7aa3d7f8b">IWPCWebSettings</a>
 

 

