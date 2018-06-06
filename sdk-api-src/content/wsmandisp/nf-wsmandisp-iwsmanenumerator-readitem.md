---
UID: NF:wsmandisp.IWSManEnumerator.ReadItem
title: IWSManEnumerator::ReadItem
author: windows-sdk-content
description: Retrieves an item from the resource and returns an XML representation of the item.
old-location: winrm\iwsmanenumerator_readitem.htm
old-project: WinRM
ms.assetid: 6b181a4b-347c-4874-969c-9ca7d36ec788
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSManEnumerator interface [Windows Remote Management],ReadItem method, IWSManEnumerator.ReadItem, IWSManEnumerator::ReadItem, ReadItem, ReadItem method [Windows Remote Management], ReadItem method [Windows Remote Management],IWSManEnumerator interface, winrm.iwsmanenumerator_readitem, wsmandisp/IWSManEnumerator::ReadItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEnumerator.ReadItem
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManEnumerator::ReadItem


## -description


Retrieves an item from the  resource and  returns an XML representation of the item.


## -parameters




### -param resource [out]

The XML representation of the item.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To start an enumeration, use <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession.Enumerate</a>. To perform a WS-Eventing:Pull operation that continues reading items in the enumeration, use <b>IWSManEnumerator.ReadItem</b>.

To limit the number of items that are read, set the <a href="https://msdn.microsoft.com/1675ba12-a0c7-4e59-a013-2109780e8afe">Session.BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.




## -see-also




<a href="https://msdn.microsoft.com/4280ecb8-2449-41bd-868a-785e8ac3b3d5">Enumerator.ReadItem</a>



<a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a>
 

 

