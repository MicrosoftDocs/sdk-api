---
UID: NF:wmp.IWMPCdromBurn.isAvailable
title: IWMPCdromBurn::isAvailable method
author: windows-driver-content
description: The isAvailable method provides information about the CD drive and media.
old-location: wmp\iwmpcdromburn_isavailable.htm
old-project: WMP
ms.assetid: 11876b73-10a1-49e2-ad45-33d9641c3647
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPCdromBurn, IWMPCdromBurn interface [Windows Media Player], isAvailable method, IWMPCdromBurn::isAvailable, IWMPCdromBurnisAvailable, isAvailable method [Windows Media Player], isAvailable method [Windows Media Player], IWMPCdromBurn interface, isAvailable,IWMPCdromBurn.isAvailable, wmp.iwmpcdromburn_isavailable, wmp/IWMPCdromBurn::isAvailable
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPCdromBurn.isAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn::isAvailable method


## -description



The <b>isAvailable</b> method provides information about the CD drive and media.




## -parameters




### -param bstrItem [in]

<b>BSTR</b> that contains one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>Burn</td>
<td>The drive is a CD burner.</td>
</tr>
<tr>
<td>Disc</td>
<td>There is a CD in the drive.</td>
</tr>
<tr>
<td>Erase</td>
<td>The CD can be erased.</td>
</tr>
<tr>
<td>Write</td>
<td>The CD can be written to.</td>
</tr>
</table>
 


### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates the result.


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




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>
 

 

