---
UID: NN:wia_xp.IWiaDataCallback
title: IWiaDataCallback
author: windows-sdk-content
description: Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.Note  For Windows Vista applications, use IWiaTransferCallback instead of IWiaDataCallback.
old-location: wia\_wia_IWiaDataCallback.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatacallback\iwiadatacallback.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWiaDataCallback, IWiaDataCallback interface [WIA], IWiaDataCallback interface [WIA],described, _wia_IWiaDataCallback, wia._wia_IWiaDataCallback, wia_xp/IWiaDataCallback
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
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IWiaDataCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaDataCallback interface


## -description


Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/en-us/library/ms629914(v=VS.85).aspx">IWiaTransferCallback</a> instead of <b>IWiaDataCallback</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaDataCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaDataCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaDataCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630156(v=VS.85).aspx">BandedDataCallback</a>
</td>
<td align="left" width="63%">
Provides data transfer status notifications. WIA data transfer methods of the <a href="https://msdn.microsoft.com/en-us/library/ms630155(v=VS.85).aspx">IWiaDataTransfer</a> interface periodically call this method. 

</td>
</tr>
</table> 


## -remarks



The <b>IWiaDataCallback</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

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
 



