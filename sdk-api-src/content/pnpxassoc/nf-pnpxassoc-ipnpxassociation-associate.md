---
UID: NF:pnpxassoc.IPNPXAssociation.Associate
title: IPNPXAssociation::Associate (pnpxassoc.h)
author: windows-sdk-content
description: Marks an association database entry as associated.
old-location: ncd\ipnpxassociation_associate.htm
tech.root: FunDisc
ms.assetid: 74d2ed38-9362-4664-9384-e773e4ec76f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Associate, Associate method, Associate method,IPNPXAssociation interface, IPNPXAssociation interface,Associate method, IPNPXAssociation.Associate, IPNPXAssociation::Associate, ncd.ipnpxassociation_associate, pnpxassoc/IPNPXAssociation::Associate
ms.topic: method
req.header: pnpxassoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - pnpxassoc.h
api_name:
 - IPNPXAssociation.Associate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPNPXAssociation::Associate


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Marks an association database entry as associated.  If there is no association database entry for the function instance, one is created; otherwise the existing entry is updated.


## -parameters




### -param pszSubcategory [in, optional]

The subcategory of the association database in which the entry is stored.   This parameter can be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -remarks



This method modifies the association database entry corresponding to the function instance from which the <a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a> interface was obtained. 

Once a device is associated, the PnP-X Service IP Bus Enumerator (IPBusEnum) sends a request to the PnP component  to create the device <a href="https://msdn.microsoft.com/en-us/library/Aa364290(v=VS.85).aspx">devnode</a>. The <b>Found New Hardware</b> wizard appears if user intervention is required to install a device driver after association.




## -see-also




<a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a>



<a href="https://msdn.microsoft.com/2024c2b8-ef47-4352-80ea-c68b22f38d4c">IPNPXDeviceAssociation::Associate</a>
 

 

