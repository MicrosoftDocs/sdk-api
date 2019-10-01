---
UID: NN:wia_xp.IWiaDevMgr
title: IWiaDevMgr (wia_xp.h)
author: windows-sdk-content
description: Applications use the IWiaDevMgr interface to create and manage image acquisition devices.
old-location: wia\_wia_IWiaDevMgr.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\iwiadevmgr.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr, IWiaDevMgr interface [WIA], IWiaDevMgr interface [WIA],described, _wia_IWiaDevMgr, wia._wia_IWiaDevMgr, wia_xp/IWiaDevMgr
ms.topic: interface
f1_keywords: 
 - "wia_xp/IWiaDevMgr"
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDevMgr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaDevMgr interface


## -description


Applications use the <b>IWiaDevMgr</b> interface to create and manage image acquisition devices. They also use it to register to receive device events.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://docs.microsoft.com/windows/desktop/wia/-wia-iwiadevmgr2">IWiaDevMgr2</a> instead of <b>IWiaDevMgr</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDevMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaDevMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaDevMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-adddevicedlg">AddDeviceDlg</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice">CreateDevice</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice">IWiaDevMgr::CreateDevice</a> creates a hierarchical tree of <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects for a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo">EnumDeviceInfo</a>
</td>
<td align="left" width="63%">
Applications use the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo">IWiaDevMgr::EnumDeviceInfo</a> method to enumerate property information for each available WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg">GetImageDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg">IWiaDevMgr::GetImageDlg</a> method displays one or more dialog boxes that enable a user to acquire an image from a WIA device and write the image to a specified file. This method combines the functionality of <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a> to completely encapsulate image acquisition within a single API call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid">RegisterEventCallbackCLSID</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid">IWiaDevMgr::RegisterEventCallbackCLSID</a> method registers an application to receive events even if the application may not be running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">RegisterEventCallbackInterface</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">IWiaDevMgr::RegisterEventCallbackInterface</a> method registers a running application WIA event notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram">RegisterEventCallbackProgram</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram">IWiaDevMgr::RegisterEventCallbackProgram</a> method registers an application to receive device events. It is primarily provided for backward compatibility with applications that were not written for WIA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">SelectDeviceDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg">IWiaDevMgr::SelectDeviceDlg</a> displays a dialog box that enables the user to select a hardware device for image acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlgid">SelectDeviceDlgID</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlgid">IWiaDevMgr::SelectDeviceDlgID</a> method displays a dialog box that enables the user to select a hardware device for image acquisition.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaDevMgr</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



