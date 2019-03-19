---
UID: NF:wmp.IWMPClosedCaption2.get_SAMILangCount
title: IWMPClosedCaption2::get_SAMILangCount (wmp.h)
author: windows-sdk-content
description: The get_SAMILangCount method retrieves the number of languages supported by the current SAMI file.
old-location: wmp\iwmpclosedcaption2_get_samilangcount.htm
tech.root: WMP
ms.assetid: 6de8bef5-f0d1-498b-a482-e3f1c3e53c24
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],get_SAMILangCount method, IWMPClosedCaption2.get_SAMILangCount, IWMPClosedCaption2::get_SAMILangCount, IWMPClosedCaption2get_SAMILangCount, get_SAMILangCount, get_SAMILangCount method [Windows Media Player], get_SAMILangCount method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_get_samilangcount, wmp/IWMPClosedCaption2::get_SAMILangCount
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
 - IWMPClosedCaption2.get_SAMILangCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption2::get_SAMILangCount


## -description



The <b>get_SAMILangCount</b> method retrieves the number of languages supported by the current SAMI file.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> containing the count.


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



This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563114(v=VS.85).aspx">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563116(v=VS.85).aspx">IWMPClosedCaption2::getSAMILangName</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563123(v=VS.85).aspx">IWMPClosedCaption::get_SAMILang</a>
 

 

