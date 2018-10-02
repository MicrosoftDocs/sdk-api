---
UID: NF:wmp.IWMPClosedCaption2.getSAMILangName
title: IWMPClosedCaption2::getSAMILangName
author: windows-sdk-content
description: The getSAMILangName method retrieves the name of a language supported by the current SAMI file.
old-location: wmp\iwmpclosedcaption2_getsamilangname.htm
tech.root: WMP
ms.assetid: f2da5045-4000-46d8-a610-f5f80cb6f713
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],getSAMILangName method, IWMPClosedCaption2.getSAMILangName, IWMPClosedCaption2::getSAMILangName, IWMPClosedCaption2getSAMILangName, getSAMILangName, getSAMILangName method [Windows Media Player], getSAMILangName method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_getsamilangname, wmp/IWMPClosedCaption2::getSAMILangName
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
 - IWMPClosedCaption2.getSAMILangName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption2::getSAMILangName


## -description



The <b>getSAMILangName</b> method retrieves the name of a language supported by the current SAMI file.




## -parameters




### -param nIndex [in]

<b>long</b> containing the index of the language name to retrieve.


### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name.


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



The languages in a SAMI file are indexed in the order shown in the file, starting with zero.

This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/21067ac1-d29e-4f1b-b123-34b24929369a">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/bcb72cf3-dad2-46b4-9652-349b804cda22">IWMPClosedCaption::get_SAMILang</a>
 

 

