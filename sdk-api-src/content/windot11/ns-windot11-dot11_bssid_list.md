---
UID: NS:windot11.DOT11_BSSID_LIST
title: DOT11_BSSID_LIST
author: windows-driver-content
description: Contains a list of basic service set (BSS) identifiers.
old-location: nwifi\dot11_bssid_list.htm
old-project: NativeWiFi
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_BSSID_LIST, DOT11_BSSID_LIST, DOT11_BSSID_LIST structure [NativeWIFI], PDOT11_BSSID_LIST, PDOT11_BSSID_LIST structure pointer [NativeWIFI], nwifi.dot11_bssid_list, windot11/DOT11_BSSID_LIST, windot11/PDOT11_BSSID_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windot11.h
req.include-header: Windot11.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_BSSID_LIST, *PDOT11_BSSID_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	windot11.h
api_name:
-	DOT11_BSSID_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DOT11_BSSID_LIST structure


## -description


The <b>DOT11_BSSID_LIST</b> structure contains a list of basic service set (BSS) identifiers.


## -struct-fields




### -field Header

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff566588">NDIS_OBJECT_HEADER</a> structure that contains the type, version, and, size information of an NDIS structure. For most <b>DOT11_BSSID_LIST</b> structures, set the <b>Type</b> member to <b>NDIS_OBJECT_TYPE_DEFAULT</b>, set the <b>Revision</b> member to <b>DOT11_BSSID_LIST_REVISION_1</b>, and set the <b>Size</b> member to <b>sizeof(DOT11_BSSID_LIST)</b>.


### -field uNumOfEntries

The number of entries in this structure. 



### -field uTotalNumOfEntries

The total number of entries supported. 



### -field BSSIDs

A list of BSS identifiers. A BSS identifier is stored as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff548681">DOT11_MAC_ADDRESS</a> type.


## -see-also




<a href="https://msdn.microsoft.com/e0321447-b89a-4f4e-929e-eb6db76f7283">WLAN_CONNECTION_PARAMETERS</a>
 

 

