---
UID: NN:wia_xp.IWiaDataCallback
title: IWiaDataCallback
author: windows-sdk-content
description: Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.Note  For Windows Vista applications, use IWiaTransferCallback instead of IWiaDataCallback.
old-location: wia\_wia_IWiaDataCallback.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatacallback\iwiadatacallback.htm
ms.author: windowssdkdev
ms.date: 05/03/2018
ms.keywords: IWiaDataCallback, IWiaDataCallback interface [WIA], IWiaDataCallback interface [WIA],described, _wia_IWiaDataCallback, wia._wia_IWiaDataCallback, wia_xp/IWiaDataCallback
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaguid.lib
-	Wiaguid.dll
api_name:
-	IWiaDataCallback
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDataCallback interface


## -description


Provides an application callback mechanism during data transfers from Windows Image Acquisition (WIA) hardware devices to applications.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/8fcaccf5-4d7b-4984-97ec-ec8c838a8360">IWiaTransferCallback</a> instead of <b>IWiaDataCallback</b>.</div><div> </div>

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
<a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">BandedDataCallback</a>
</td>
<td align="left" width="63%">
Provides data transfer status notifications. WIA data transfer methods of the <a href="https://msdn.microsoft.com/565e48b7-30c5-4c8b-ae4a-071c2e90b2f9">IWiaDataTransfer</a> interface periodically call this method. 

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
 



