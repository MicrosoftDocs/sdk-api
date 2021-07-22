---
UID: NF:wuapi.IUpdateLockdown.LockDown
title: IUpdateLockdown::LockDown (wuapi.h)
description: Restricts access to the methods and properties of the object that implements this method.
helpviewer_keywords: ["IUpdateLockdown interface [Windows Update Agent]","Lockdown method","IUpdateLockdown.LockDown","IUpdateLockdown::LockDown","IUpdateLockdown::Lockdown","LockDown","Lockdown method [Windows Update Agent]","Lockdown method [Windows Update Agent]","IUpdateLockdown interface","wua.iupdatelockdown_lockdown","wuapi/IUpdateLockdown::Lockdown"]
old-location: wua\iupdatelockdown_lockdown.htm
tech.root: wua
ms.assetid: 3d3be6f8-acdc-4cef-a0bc-6572a5b315d8
ms.date: 12/05/2018
ms.keywords: IUpdateLockdown interface [Windows Update Agent],Lockdown method, IUpdateLockdown.LockDown, IUpdateLockdown::LockDown, IUpdateLockdown::Lockdown, LockDown, Lockdown method [Windows Update Agent], Lockdown method [Windows Update Agent],IUpdateLockdown interface, wua.iupdatelockdown_lockdown, wuapi/IUpdateLockdown::Lockdown
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateLockdown::LockDown
 - wuapi/IUpdateLockdown::LockDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateLockdown.Lockdown
---

# IUpdateLockdown::LockDown


## -description

Restricts access to the methods and properties of the object that implements this method.

## -parameters

### -param flags [in]

The option to restrict access to various Windows Update Agent (WUA) objects from the Windows Update website. 

Setting this parameter to  <b>uloForWebsiteAccess</b> or to 1 (one) restricts access to the WUA interfaces that implement the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatelockdown">IUpdateLockdown</a> interface.

For a list of the methods and properties that the WUA interfaces restrict when this value is specified, see the "Remarks" section.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following table identifies the interfaces that implement the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatelockdown">IUpdateLockdown</a> interface.

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
<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdateDownloader</a>
</td>
<td>
<dl>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-download">BeginDownload</a>
</dd>
<dd>
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">Download</a>
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

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatelockdown">IUpdateLockdown</a>