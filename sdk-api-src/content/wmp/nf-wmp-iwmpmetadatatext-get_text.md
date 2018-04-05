---
UID: NF:wmp.IWMPMetadataText.get_text
title: IWMPMetadataText::get_text method
author: windows-driver-content
description: The get_text method retrieves the metadata text.
old-location: wmp\iwmpmetadatatext_get_text.htm
old-project: WMP
ms.assetid: 88aeb4bb-87e1-413d-888b-608fa349ebf5
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPMetadataText, IWMPMetadataText interface [Windows Media Player], get_text method, IWMPMetadataText::get_text, IWMPMetadataTextget_text, get_text method [Windows Media Player], get_text method [Windows Media Player], IWMPMetadataText interface, get_text,IWMPMetadataText.get_text, wmp.iwmpmetadatatext_get_text, wmp/IWMPMetadataText::get_text
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
-	IWMPMetadataText.get_text
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMetadataText::get_text method


## -description



The <b>get_text</b> method retrieves the metadata text.




## -parameters




### -param pbstrText [out]

Pointer to a <b>BSTR</b> containing the text.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/15d040fa-6c14-41ff-bd21-a8991c17681d">IWMPMetadataText Interface</a>
 

 

