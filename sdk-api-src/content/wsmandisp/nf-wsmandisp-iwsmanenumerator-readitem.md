---
UID: NF:wsmandisp.IWSManEnumerator.ReadItem
title: IWSManEnumerator::ReadItem (wsmandisp.h)
author: windows-sdk-content
description: Retrieves an item from the resource and returns an XML representation of the item.
old-location: winrm\iwsmanenumerator_readitem.htm
tech.root: winrm
ms.assetid: 6b181a4b-347c-4874-969c-9ca7d36ec788
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSManEnumerator interface [Windows Remote Management],ReadItem method, IWSManEnumerator.ReadItem, IWSManEnumerator::ReadItem, ReadItem, ReadItem method [Windows Remote Management], ReadItem method [Windows Remote Management],IWSManEnumerator interface, winrm.iwsmanenumerator_readitem, wsmandisp/IWSManEnumerator::ReadItem
ms.topic: method
f1_keywords: 
 - "wsmandisp/IWSManEnumerator.ReadItem"
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEnumerator.ReadItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



To start an enumeration, use <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">IWSManSession.Enumerate</a>. To perform a WS-Eventing:Pull operation that continues reading items in the enumeration, use <b>IWSManEnumerator.ReadItem</b>.

To limit the number of items that are read, set the <a href="https://docs.microsoft.com/windows/desktop/WinRM/session-batchitems">Session.BatchItems</a> property.

Be aware that freeing the enumeration object clears pending enumeration requests.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinRM/enumerator-readitem">Enumerator.ReadItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanenumerator">IWSManEnumerator</a>
 

 

