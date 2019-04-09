---
UID: NF:wmp.IWMPErrorItem.get_errorContext
title: IWMPErrorItem::get_errorContext (wmp.h)
author: windows-sdk-content
description: The get_errorContext method retrieves a value indicating the context of the error.
old-location: wmp\iwmperroritem_get_errorcontext.htm
tech.root: WMP
ms.assetid: 575f14e7-7a5b-4000-9957-253c40b1ef62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_errorContext method, IWMPErrorItem.get_errorContext, IWMPErrorItem::get_errorContext, IWMPErrorItemget_errorContext, get_errorContext, get_errorContext method [Windows Media Player], get_errorContext method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_errorcontext, wmp/IWMPErrorItem::get_errorContext
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
 - IWMPErrorItem.get_errorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPErrorItem::get_errorContext


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563273(v=VS.85).aspx">IWMPErrorItem Interface</a>
 

 

