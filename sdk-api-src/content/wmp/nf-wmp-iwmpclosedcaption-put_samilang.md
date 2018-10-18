---
UID: NF:wmp.IWMPClosedCaption.put_SAMILang
title: IWMPClosedCaption::put_SAMILang
author: windows-sdk-content
description: The put_SAMILang method specifies the language displayed for closed captioning.
old-location: wmp\iwmpclosedcaption_put_samilang.htm
tech.root: WMP
ms.assetid: 2027d8cd-2528-45ad-9f36-f03cc3001ba7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPClosedCaption interface [Windows Media Player],put_SAMILang method, IWMPClosedCaption.put_SAMILang, IWMPClosedCaption::put_SAMILang, IWMPClosedCaptionput_SAMILang, put_SAMILang, put_SAMILang method [Windows Media Player], put_SAMILang method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_put_samilang, wmp/IWMPClosedCaption::put_SAMILang
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
 - IWMPClosedCaption.put_SAMILang
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption::put_SAMILang


## -description



The <b>put_SAMILang</b> method specifies the language displayed for closed captioning.




## -parameters




### -param bstrSAMILang [in]

Pointer to a <b>BSTR</b> containing the language.


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



A SAMI file can contain text for one or many languages. The languages available for closed captioning are defined between the &lt;STYLE&gt; and &lt;/STYLE&gt; tags in the SAMI file. A language identifier is specified with a unique alphanumeric string that is preceded by a period (.). The name specified for a language can be any string. For example, the following could be used to define US English:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```


If no SAMI language is specified, the first language defined in the SAMI file is used by default.

The value you specify using <b>put_SAMILang</b> must match the <b>Name</b> attribute in the language specifier.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/bcb72cf3-dad2-46b4-9652-349b804cda22">IWMPClosedCaption::get_SAMILang</a>
 

 

