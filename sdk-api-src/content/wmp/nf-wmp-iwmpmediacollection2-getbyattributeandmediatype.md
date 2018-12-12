---
UID: NF:wmp.IWMPMediaCollection2.getByAttributeAndMediaType
title: IWMPMediaCollection2::getByAttributeAndMediaType
author: windows-sdk-content
description: The getByAttributeAndMediaType method retrieves a pointer to an IWMPPlaylist interface. This interface represents a playlist that contains media items that have a specified attribute and media type.
old-location: wmp\iwmpmediacollection2_getbyattributeandmediatype.htm
tech.root: WMP
ms.assetid: cf925189-1f68-499c-9c98-063a0367dd3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMediaCollection2 interface [Windows Media Player],getByAttributeAndMediaType method, IWMPMediaCollection2.getByAttributeAndMediaType, IWMPMediaCollection2::getByAttributeAndMediaType, IWMPMediaCollection2getByAttributeAndMediaType, getByAttributeAndMediaType, getByAttributeAndMediaType method [Windows Media Player], getByAttributeAndMediaType method [Windows Media Player],IWMPMediaCollection2 interface, wmp.iwmpmediacollection2_getbyattributeandmediatype, wmp/IWMPMediaCollection2::getByAttributeAndMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPMediaCollection2.getByAttributeAndMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection2::getByAttributeAndMediaType


## -description



The <b>getByAttributeAndMediaType</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface represents a playlist that contains media items that have a specified attribute and media type.




## -parameters




### -param bstrAttribute [in]

String that contains the specified attribute.


### -param bstrValue [in]

String that contains the specified value for the attribute that is specified in <i>bstrAttribute</i>.


### -param bstrMediaType [in]

String that contains the specified media type.


### -param ppMediaItems [out]

Address of a variable that receives a pointer to an <b>IWMPPlaylist</b> interface for the retrieved playlist.


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



<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563406(v=VS.85).aspx">IWMPMediaCollection2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>
 

 

