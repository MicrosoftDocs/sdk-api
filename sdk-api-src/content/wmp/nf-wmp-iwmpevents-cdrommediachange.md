---
UID: NF:wmp.IWMPEvents.CdromMediaChange
title: IWMPEvents::CdromMediaChange (wmp.h)
author: windows-sdk-content
description: The CdromMediaChange event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.
old-location: wmp\iwmpevents_iwmpevents__cdrommediachange.htm
tech.root: WMP
ms.assetid: 019ab066-ae2b-4517-bc1c-d96bb6e8e15e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CdromMediaChange, CdromMediaChange method [Windows Media Player], CdromMediaChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CdromMediaChange method, IWMPEvents.CdromMediaChange, IWMPEvents::CdromMediaChange, IWMPEventsCdromMediaChange, wmp.iwmpevents_iwmpevents__cdrommediachange, wmp/IWMPEvents::CdromMediaChange
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.CdromMediaChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::CdromMediaChange


## -description



The <b>CdromMediaChange</b> event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.




## -parameters




### -param CdromNum [in]

Specifies the index of the CD or DVD drive.


## -returns



This method does not return a value.




## -remarks



The index of the CD drive corresponds to the index of a <b>Cdrom</b> object in the <b>IWMPCdromCollection</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563097(v=VS.85).aspx">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563310(v=VS.85).aspx">IWMPEvents Interface</a>
 

 

