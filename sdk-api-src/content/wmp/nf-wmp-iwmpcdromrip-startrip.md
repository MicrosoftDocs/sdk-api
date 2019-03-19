---
UID: NF:wmp.IWMPCdromRip.startRip
title: IWMPCdromRip::startRip (wmp.h)
author: windows-sdk-content
description: The startRip method rips the CD.
old-location: wmp\iwmpcdromrip_startrip.htm
tech.root: WMP
ms.assetid: 88ba1e83-a3c5-4922-8c58-37993ccb4afc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCdromRip interface [Windows Media Player],startRip method, IWMPCdromRip.startRip, IWMPCdromRip::startRip, IWMPCdromRipstartRip, startRip, startRip method [Windows Media Player], startRip method [Windows Media Player],IWMPCdromRip interface, wmp.iwmpcdromrip_startrip, wmp/IWMPCdromRip::startRip
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromRip.startRip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCdromRip::startRip


## -description



The <b>startRip</b> method rips the CD.




## -parameters






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



<b>Windows Media Player 10 Mobile: </b>This method is not supported.

Ripping a CD by using the <b>IWMPCdromRip</b> interface has the same effect as ripping music by using the Windows Media Player user interface. Ripped content is automatically added to the library according to the user's preferences. For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563102(v=VS.85).aspx">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563106(v=VS.85).aspx">IWMPCdromRip::stopRip</a>



<a href="https://msdn.microsoft.com/f5c1b5bf-d616-48cb-8690-e0237c56e402">Ripping a CD</a>
 

 

