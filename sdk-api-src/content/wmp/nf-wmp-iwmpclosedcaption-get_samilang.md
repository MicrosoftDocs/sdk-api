---
UID: NF:wmp.IWMPClosedCaption.get_SAMILang
title: IWMPClosedCaption::get_SAMILang
author: windows-sdk-content
description: The get_SAMILang method retrieves the language displayed for closed captioning.
old-location: wmp\iwmpclosedcaption_get_samilang.htm
old-project: WMP
ms.assetid: bcb72cf3-dad2-46b4-9652-349b804cda22
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_SAMILang method, IWMPClosedCaption.get_SAMILang, IWMPClosedCaption::get_SAMILang, IWMPClosedCaptionget_SAMILang, get_SAMILang, get_SAMILang method [Windows Media Player], get_SAMILang method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_samilang, wmp/IWMPClosedCaption::get_SAMILang
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPClosedCaption.get_SAMILang
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPClosedCaption::get_SAMILang


## -description



The <b>get_SAMILang</b> method retrieves the language displayed for closed captioning.




## -parameters




### -param pbstrSAMILang [out]

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



A SAMI file can contain text for one or many languages. The languages available for closed captioning are defined between the &lt;STYLE&gt; and &lt;/STYLE&gt; tags in the SAMI file. A language identifier is specified by a unique alphanumeric string that is preceded by a period (.). The name specified for a language can be any string. For example, the following could be used to define US English:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
</pre>
</td>
</tr>
</table></span></div>
If no SAMI language is specified, the first language defined in the SAMI file is used by default.

The value you specify using <b>put_SAMILang</b> must match the <b>Name</b> attribute in the language specifier.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/2027d8cd-2528-45ad-9f36-f03cc3001ba7">IWMPClosedCaption::put_SAMILang</a>
 

 

