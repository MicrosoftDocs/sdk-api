---
UID: NF:wmp.IWMPLibrary2.getItemInfo
title: IWMPLibrary2::getItemInfo
author: windows-driver-content
description: The getItemInfo method retrieves the value of the LibraryID attribute.
old-location: wmp\iwmplibrary2_getiteminfo.htm
old-project: WMP
ms.assetid: 38de9e72-b942-4c09-be9e-ff9f345c778d
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPLibrary2 interface [Windows Media Player],getItemInfo method, IWMPLibrary2.getItemInfo, IWMPLibrary2::getItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPLibrary2 interface, wmp.iwmplibrary2_getiteminfo, wmp/IWMPLibrary2::getItemInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
-	wmp.h
api_name:
-	IWMPLibrary2.getItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPLibrary2::getItemInfo


## -description


The <b>getItemInfo</b> method retrieves the value of the <b>LibraryID</b> attribute.


## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name. Set the value of this parameter to "LibraryID".


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that receives the value of the <b>LibraryID</b> attribute.


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



The <b>LibraryID</b> attribute retrieved by this method is the same as the <b>LibraryID</b> attribute that <a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">IWMPMedia::getItemInfo</a> retrieves for each media item in the library.




## -see-also




<a href="https://msdn.microsoft.com/028250e7-7415-4643-b798-af0112c1ea93">IWMPLibrary2</a>
 

 

