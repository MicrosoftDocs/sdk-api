---
UID: NF:wmp.IWMPSettings2.get_mediaAccessRights
title: IWMPSettings2::get_mediaAccessRights method
author: windows-driver-content
description: The get_mediaAccessRights method retrieves a value indicating the permissions currently granted for library access.
old-location: wmp\iwmpsettings2_get_mediaaccessrights.htm
old-project: WMP
ms.assetid: 07ca80a3-5175-4b1f-b83c-0df41a010cbf
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPSettings2, IWMPSettings2 interface [Windows Media Player], get_mediaAccessRights method, IWMPSettings2::get_mediaAccessRights, IWMPSettings2get_mediaAccessRights, get_mediaAccessRights method [Windows Media Player], get_mediaAccessRights method [Windows Media Player], IWMPSettings2 interface, get_mediaAccessRights,IWMPSettings2.get_mediaAccessRights, wmp.iwmpsettings2_get_mediaaccessrights, wmp/IWMPSettings2::get_mediaAccessRights
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPSettings2.get_mediaAccessRights
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings2::get_mediaAccessRights method


## -description



The <b>get_mediaAccessRights</b> method retrieves a value indicating the permissions currently granted for library access.




## -parameters




### -param pbstrRights [out]

Pointer to a <b>BSTR</b> containing one of the following values.

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
<td>none</td>
<td>Current item access rights only.</td>
</tr>
<tr>
<td>read</td>
<td>Read access rights only.</td>
</tr>
<tr>
<td>full</td>
<td>Read/Write access rights.</td>
</tr>
</table>
 


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



A webpage must first request permission from the user to read information from or write data to the library. This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted. To obtain access rights, the application calls <b>IWMPSettings2::get_requestMediaAccessRights</b>, passing a parameter that specifies the desired access rights level.

Applications running on the user's computer always have full access rights.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing the string "full".




## -see-also




<a href="https://msdn.microsoft.com/0fb0c7be-015e-4081-8467-c382e0858195">IWMPSettings2 Interface</a>



<a href="https://msdn.microsoft.com/925a4c0b-d613-4248-a341-bfc51d02cb85">IWMPSettings2::requestMediaAccessRights</a>
 

 

