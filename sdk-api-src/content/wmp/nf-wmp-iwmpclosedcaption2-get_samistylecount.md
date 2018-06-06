---
UID: NF:wmp.IWMPClosedCaption2.get_SAMIStyleCount
title: IWMPClosedCaption2::get_SAMIStyleCount
author: windows-sdk-content
description: The get_SAMIStyleCount method retrieves the number of styles supported by the current SAMI file.
old-location: wmp\iwmpclosedcaption2_get_samistylecount.htm
old-project: WMP
ms.assetid: e31985e3-e5ab-4a29-b0d7-9a1cda58bca1
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],get_SAMIStyleCount method, IWMPClosedCaption2.get_SAMIStyleCount, IWMPClosedCaption2::get_SAMIStyleCount, IWMPClosedCaption2get_SAMIStyleCount, get_SAMIStyleCount, get_SAMIStyleCount method [Windows Media Player], get_SAMIStyleCount method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_get_samistylecount, wmp/IWMPClosedCaption2::get_SAMIStyleCount
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
 - IWMPClosedCaption2.get_SAMIStyleCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPClosedCaption2::get_SAMIStyleCount


## -description



The <b>get_SAMIStyleCount</b> method retrieves the number of styles supported by the current SAMI file.




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



<a href="https://msdn.microsoft.com/21067ac1-d29e-4f1b-b123-34b24929369a">IWMPClosedCaption2 Interface</a>



<a href="https://msdn.microsoft.com/0dfdbe70-2aa8-4cae-8886-6b770707652e">IWMPClosedCaption2::getSAMIStyleName</a>



<a href="https://msdn.microsoft.com/27040145-af7a-4d09-9c80-e0907df08f01">IWMPClosedCaption::get_SAMIStyle</a>
 

 

