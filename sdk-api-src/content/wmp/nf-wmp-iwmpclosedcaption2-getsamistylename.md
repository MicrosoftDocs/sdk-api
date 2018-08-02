---
UID: NF:wmp.IWMPClosedCaption2.getSAMIStyleName
title: IWMPClosedCaption2::getSAMIStyleName
author: windows-sdk-content
description: The getSAMIStyleName method retrieves the name of a style supported by the current SAMI file.
old-location: wmp\iwmpclosedcaption2_getsamistylename.htm
old-project: WMP
ms.assetid: 0dfdbe70-2aa8-4cae-8886-6b770707652e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],getSAMIStyleName method, IWMPClosedCaption2.getSAMIStyleName, IWMPClosedCaption2::getSAMIStyleName, IWMPClosedCaption2getSAMIStyleName, getSAMIStyleName, getSAMIStyleName method [Windows Media Player], getSAMIStyleName method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_getsamistylename, wmp/IWMPClosedCaption2::getSAMIStyleName
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
 - IWMPClosedCaption2.getSAMIStyleName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPClosedCaption2::getSAMIStyleName


## -description



The <b>getSAMIStyleName</b> method retrieves the name of a style supported by the current SAMI file.




## -parameters




### -param nIndex [in]

<b>long</b> containing the index of the style name to retrieve.


### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name of the style as specified in the SAMI file.


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



The styles in a SAMI file are indexed in the order shown in the file, starting with zero.

This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/21067ac1-d29e-4f1b-b123-34b24929369a">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/27040145-af7a-4d09-9c80-e0907df08f01">IWMPClosedCaption::get_SAMIStyle</a>
 

 

