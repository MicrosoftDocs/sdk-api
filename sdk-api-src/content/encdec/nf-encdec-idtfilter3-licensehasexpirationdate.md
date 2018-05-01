---
UID: NF:encdec.IDTFilter3.LicenseHasExpirationDate
title: IDTFilter3::LicenseHasExpirationDate method
author: windows-driver-content
description: The LicenseHasExpirationDate method queries whether the license for the content has an expiration date.
old-location: mstv\idtfilter3_licensehasexpirationdate.htm
old-project: mstv
ms.assetid: 712be51a-27ed-4ede-bef6-9223c57f446f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDTFilter3, IDTFilter3 interface [Microsoft TV Technologies], LicenseHasExpirationDate method, IDTFilter3::LicenseHasExpirationDate, IDTFilter3LicenseHasExpirationDate, LicenseHasExpirationDate method [Microsoft TV Technologies], LicenseHasExpirationDate method [Microsoft TV Technologies], IDTFilter3 interface, LicenseHasExpirationDate,IDTFilter3.LicenseHasExpirationDate, encdec/IDTFilter3::LicenseHasExpirationDate, mstv.idtfilter3_licensehasexpirationdate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IDTFilter3.LicenseHasExpirationDate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilter3::LicenseHasExpirationDate method


## -description


The <b>LicenseHasExpirationDate</b> method queries whether the license for the content has an expiration date.


## -parameters




### -param pfLicenseHasExpirationDate [out]

Receives a Boolean value. If <b>TRUE</b>, the license has an expiration date. If <b>FALSE</b>, the license does not expire.


## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/88e42006-c387-41b5-a013-e968da0d918b">IDTFilter3 Interface</a>
 

 

