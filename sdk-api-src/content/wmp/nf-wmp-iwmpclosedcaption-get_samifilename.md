---
UID: NF:wmp.IWMPClosedCaption.get_SAMIFileName
title: IWMPClosedCaption::get_SAMIFileName
author: windows-sdk-content
description: The get_SAMIFileName method retrieves the name of the file containing the information needed for closed captioning.
old-location: wmp\iwmpclosedcaption_get_samifilename.htm
old-project: WMP
ms.assetid: 2f09df76-3bfc-48ce-881f-c905656ecbbf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_SAMIFileName method, IWMPClosedCaption.get_SAMIFileName, IWMPClosedCaption::get_SAMIFileName, IWMPClosedCaptionget_SAMIFileName, get_SAMIFileName, get_SAMIFileName method [Windows Media Player], get_SAMIFileName method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_samifilename, wmp/IWMPClosedCaption::get_SAMIFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPClosedCaption.get_SAMIFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPClosedCaption::get_SAMIFileName


## -description



The <b>get_SAMIFileName</b> method retrieves the name of the file containing the information needed for closed captioning.




## -parameters




### -param pbstrSAMIFileName [out]

Pointer to a <b>BSTR</b> containing the name of the Synchronized Accessible Media Interchange (SAMI) file.


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



The SAMI file must use an .smi or .sami file name extension.

If you do not specify a value by using <b>IWMPClosedCaption::put_SAMIFileName</b>, the <b>get_SAMIFileName</b> method retrieves a <b>BSTR</b> containing the default file or URL associated with the current media item. This association can occur when a SAMI file is specified by using the <i>sami</i> URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension). If there is no default SAMI file associated with the current media, <b>get_SAMIFileName</b> retrieves an empty string ("").

If you want Windows Media Player to use the default SAMI file associated with a particular media item, call <b>IWMPClosedCaption::put_SAMIFileName</b> using an empty string ("") before you play the next media item.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/ebc05983-3375-4ace-b192-f427b9685310">IWMPClosedCaption::put_SAMIFileName</a>



<a href="https://msdn.microsoft.com/e6e21995-5dbd-4893-a9f2-6ce918d3fbc4">IWMPCore::close</a>
 

 

