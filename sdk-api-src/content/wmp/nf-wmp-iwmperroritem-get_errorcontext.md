---
UID: NF:wmp.IWMPErrorItem.get_errorContext
title: IWMPErrorItem::get_errorContext method
author: windows-driver-content
description: The get_errorContext method retrieves a value indicating the context of the error.
old-location: wmp\iwmperroritem_get_errorcontext.htm
old-project: WMP
ms.assetid: 575f14e7-7a5b-4000-9957-253c40b1ef62
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPErrorItem, IWMPErrorItem interface [Windows Media Player], get_errorContext method, IWMPErrorItem::get_errorContext, IWMPErrorItemget_errorContext, get_errorContext method [Windows Media Player], get_errorContext method [Windows Media Player], IWMPErrorItem interface, get_errorContext,IWMPErrorItem.get_errorContext, wmp.iwmperroritem_get_errorcontext, wmp/IWMPErrorItem::get_errorContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPErrorItem.get_errorContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPErrorItem::get_errorContext method


## -description



The <b>get_errorContext</b> method retrieves a value indicating the context of the error.




## -parameters




### -param pvarContext [out]

Pointer to a <b>VARIANT</b> containing the error context.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The error context is information that is used by Microsoft to provide additional information for technical support personnel.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT</b> with the <b>vt</b> field set to VT_EMPTY.




## -see-also




<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>
 

 

