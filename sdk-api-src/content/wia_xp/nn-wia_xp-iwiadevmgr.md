---
UID: NN:wia_xp.IWiaDevMgr
title: IWiaDevMgr
author: windows-driver-content
description: Applications use the IWiaDevMgr interface to create and manage image acquisition devices.
old-location: wia\_wia_IWiaDevMgr.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\iwiadevmgr.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IWiaDevMgr, IWiaDevMgr interface [WIA], IWiaDevMgr interface [WIA], described, _wia_IWiaDevMgr, wia._wia_IWiaDevMgr, wia_xp/IWiaDevMgr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaservc.dll
api_name:
-	IWiaDevMgr
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDevMgr interface


## -description


Applications use the <b>IWiaDevMgr</b> interface to create and manage image acquisition devices. They also use it to register to receive device events.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38">IWiaDevMgr2</a> instead of <b>IWiaDevMgr</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDevMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaDevMgr</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/602ff6f6-184a-4126-8b02-5f9054852b26">AddDeviceDlg</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c1e264-7f60-49d7-ba2c-2f06919fc807">CreateDevice</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d3c1e264-7f60-49d7-ba2c-2f06919fc807">IWiaDevMgr::CreateDevice</a> creates a hierarchical tree of <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects for a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29a6b2c0-2424-411a-a3fb-4518b7d6de3b">EnumDeviceInfo</a>
</td>
<td align="left" width="63%">
Applications use the <a href="https://msdn.microsoft.com/29a6b2c0-2424-411a-a3fb-4518b7d6de3b">IWiaDevMgr::EnumDeviceInfo</a> method to enumerate property information for each available WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3cf7039-54e3-46b3-bb19-6192ec0f28ef">GetImageDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f3cf7039-54e3-46b3-bb19-6192ec0f28ef">IWiaDevMgr::GetImageDlg</a> method displays one or more dialog boxes that enable a user to acquire an image from a WIA device and write the image to a specified file. This method combines the functionality of <a href="https://msdn.microsoft.com/5c58b0f9-42a9-4d20-97a5-526b6937d495">IWiaDevMgr::SelectDeviceDlg</a> to completely encapsulate image acquisition within a single API call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71f1f7f9-583a-423c-bf96-2c2596808079">RegisterEventCallbackCLSID</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/71f1f7f9-583a-423c-bf96-2c2596808079">IWiaDevMgr::RegisterEventCallbackCLSID</a> method registers an application to receive events even if the application may not be running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81a5bb61-5ec6-4c0b-8627-faccaf54d05a">RegisterEventCallbackInterface</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/81a5bb61-5ec6-4c0b-8627-faccaf54d05a">IWiaDevMgr::RegisterEventCallbackInterface</a> method registers a running application WIA event notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177438ff-afeb-4499-9870-647c49209a6e">RegisterEventCallbackProgram</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/177438ff-afeb-4499-9870-647c49209a6e">IWiaDevMgr::RegisterEventCallbackProgram</a> method registers an application to receive device events. It is primarily provided for backward compatibility with applications that were not written for WIA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c58b0f9-42a9-4d20-97a5-526b6937d495">SelectDeviceDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5c58b0f9-42a9-4d20-97a5-526b6937d495">IWiaDevMgr::SelectDeviceDlg</a> displays a dialog box that enables the user to select a hardware device for image acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19441129-0718-4293-905e-85c8c6fd488f">SelectDeviceDlgID</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/19441129-0718-4293-905e-85c8c6fd488f">IWiaDevMgr::SelectDeviceDlgID</a> method displays a dialog box that enables the user to select a hardware device for image acquisition.

</td>
</tr>
</table> 


## -remarks



The <b>IWiaDevMgr</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 



