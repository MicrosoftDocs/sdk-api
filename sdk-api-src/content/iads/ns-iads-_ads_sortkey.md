---
UID: NS:iads._ads_sortkey
title: "_ads_sortkey"
author: windows-driver-content
description: The ADS_SORTKEY structure specifies how to sort a query.
old-location: adsi\ads_sortkey.htm
old-project: ADSI
ms.assetid: e4fe499a-4f81-4b92-bf50-b4124ae6e4a3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PADS_SORTKEY, ADS_SORTKEY, ADS_SORTKEY structure [ADSI], PADS_SORTKEY, PADS_SORTKEY structure pointer [ADSI], _ads_sortkey, _ds_ads_sortkey, adsi.ads__sortkey, adsi.ads_sortkey, iads/ADS_SORTKEY, iads/PADS_SORTKEY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADS_SORTKEY, *PADS_SORTKEY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_SORTKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ads_sortkey structure


## -description


The <b>ADS_SORTKEY</b> structure specifies how to sort a query.


## -struct-fields




### -field pszAttrType

The null-terminated Unicode string that contains the attribute type.


### -field pszReserved

Reserved.


### -field fReverseorder

Reverse the order of the sorted results.


## -remarks



In Active Directory, if <b>TRUE</b>, the <b>fReverseorder</b> member specifies that the sort results be ordered from the lowest to the highest.

When using the LDAP system provider, the <b>pszReserved</b> member corresponds to the <b>sk_matchruleoid</b> of the <a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a> structure and may be set to a NULL-terminated string that specifies the object identifier (OID) of the matching rule for the sort.  For more information, see <b>LDAPSortKey</b>.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

