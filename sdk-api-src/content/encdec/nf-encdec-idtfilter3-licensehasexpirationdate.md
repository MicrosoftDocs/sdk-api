---
UID: NF:encdec.IDTFilter3.LicenseHasExpirationDate
title: IDTFilter3::LicenseHasExpirationDate (encdec.h)
description: The LicenseHasExpirationDate method queries whether the license for the content has an expiration date.
helpviewer_keywords: ["IDTFilter3 interface [Microsoft TV Technologies]","LicenseHasExpirationDate method","IDTFilter3.LicenseHasExpirationDate","IDTFilter3::LicenseHasExpirationDate","IDTFilter3LicenseHasExpirationDate","LicenseHasExpirationDate","LicenseHasExpirationDate method [Microsoft TV Technologies]","LicenseHasExpirationDate method [Microsoft TV Technologies]","IDTFilter3 interface","encdec/IDTFilter3::LicenseHasExpirationDate","mstv.idtfilter3_licensehasexpirationdate"]
old-location: mstv\idtfilter3_licensehasexpirationdate.htm
tech.root: mstv
ms.assetid: 712be51a-27ed-4ede-bef6-9223c57f446f
ms.date: 12/05/2018
ms.keywords: IDTFilter3 interface [Microsoft TV Technologies],LicenseHasExpirationDate method, IDTFilter3.LicenseHasExpirationDate, IDTFilter3::LicenseHasExpirationDate, IDTFilter3LicenseHasExpirationDate, LicenseHasExpirationDate, LicenseHasExpirationDate method [Microsoft TV Technologies], LicenseHasExpirationDate method [Microsoft TV Technologies],IDTFilter3 interface, encdec/IDTFilter3::LicenseHasExpirationDate, mstv.idtfilter3_licensehasexpirationdate
f1_keywords:
- encdec/IDTFilter3.LicenseHasExpirationDate
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- EncDec.h
api_name:
- IDTFilter3.LicenseHasExpirationDate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter3::LicenseHasExpirationDate


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter3">IDTFilter3 Interface</a>
 

 

