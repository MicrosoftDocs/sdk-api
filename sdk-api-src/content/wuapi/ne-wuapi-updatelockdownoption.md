---
UID: NE:wuapi.tagUpdateLockdownOption
title: UpdateLockdownOption (wuapi.h)
description: Defines the functionality that the Windows Update Agent (WUA) object can access from Windows Update.
helpviewer_keywords: ["UpdateLockdownOption","UpdateLockdownOption enumeration [Windows Update Agent]","uloForWebsiteAccess","wua.updatelockdownoption","wuapi/UpdateLockdownOption","wuapi/uloForWebsiteAccess"]
old-location: wua\updatelockdownoption.htm
tech.root: wua
ms.assetid: 6e664485-d26f-4702-9190-9440b13c60b5
ms.date: 12/05/2018
ms.keywords: UpdateLockdownOption, UpdateLockdownOption enumeration [Windows Update Agent], uloForWebsiteAccess, wua.updatelockdownoption, wuapi/UpdateLockdownOption, wuapi/uloForWebsiteAccess
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UpdateLockdownOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateLockdownOption
 - wuapi/tagUpdateLockdownOption
 - UpdateLockdownOption
 - wuapi/UpdateLockdownOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateLockdownOption
---

# UpdateLockdownOption enumeration


## -description

Defines the functionality that the Windows Update Agent (WUA) object can access from Windows Update.

## -enum-fields

### -field uloForWebsiteAccess:0x1

If access is from Windows Update, restrict access to the WUA interfaces that implement the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatelockdown">IUpdateLockdown</a> interface.

## -remarks

In the following table, the first column lists the interfaces that  implement the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatelockdown">IUpdateLockdown</a> interface. The second column lists the methods and properties that are restricted by the WUA interfaces when a value is specified for <b>uloForWebsiteAccess</b>.

<table>
<tr>
<th>WUA object</th>
<th>Restricted methods and properties</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates">IAutomaticUpdates</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-pause">Pause</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-resume">Resume</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings-save">Save</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-accepteula">AcceptEula</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-copyfromcache">CopyFromCache</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate2-copytocache">CopyToCache</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloader">IUpdateDownloader</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-download">Download</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">BeginDownload</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-enddownload">EndDownload</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-get_isforced">IsForced</a> (cannot set)</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">BeginInstall</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">BeginUninstall</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-endinstall">EndInstall</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-enduninstall">EndUninstall</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-install">Install</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-get_isforced">IsForced</a> (cannot set)</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-uninstall">Uninstall</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice">AddScanPackageService</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-removeservice">RemoveService</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-setoption">SetOption</a>
</dd>
</dl>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_address">Address</a> (cannot set)</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_autodetect">AutoDetect</a> (cannot set)</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_bypasslist">BypassList</a> (cannot set)</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal">BypassProxyOnLocal</a> (cannot set)</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-setpassword">SetPassword</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_username">UserName</a> (cannot set)</dd>
</dl>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatelockdown-lockdown">IUpdateLockdown::LockDown</a>
