---
UID: NS:wlanapi._WLAN_COUNTRY_OR_REGION_STRING_LIST
title: WLAN_COUNTRY_OR_REGION_STRING_LIST (wlanapi.h)
author: windows-sdk-content
description: Contains a list of supported country or region strings.
old-location: nwifi\wlan_country_or_region_string_list.htm
tech.root: NativeWiFi
ms.assetid: 64343c1f-3543-406f-a64c-94196b8aa17e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWLAN_COUNTRY_OR_REGION_STRING_LIST, PWLAN_COUNTRY_OR_REGION_STRING_LIST, PWLAN_COUNTRY_OR_REGION_STRING_LIST structure pointer [NativeWIFI], WLAN_COUNTRY_OR_REGION_STRING_LIST, WLAN_COUNTRY_OR_REGION_STRING_LIST structure [NativeWIFI], nwifi.wlan_country_or_region_string_list, wlanapi/PWLAN_COUNTRY_OR_REGION_STRING_LIST, wlanapi/WLAN_COUNTRY_OR_REGION_STRING_LIST"
ms.topic: struct
f1_keywords: 
 - "wlanapi/WLAN_COUNTRY_OR_REGION_STRING_LIST"
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_COUNTRY_OR_REGION_STRING_LIST
targetos: Windows
req.typenames: WLAN_COUNTRY_OR_REGION_STRING_LIST, *PWLAN_COUNTRY_OR_REGION_STRING_LIST
req.redist: 
ms.custom: 19H1
---

# WLAN_COUNTRY_OR_REGION_STRING_LIST structure


## -description


A <b>WLAN_COUNTRY_OR_REGION_STRING_LIST</b> structure contains a list of supported country or region strings.


## -struct-fields




### -field dwNumberOfItems

Indicates the number of supported country or region strings.


### -field pCountryOrRegionStringList.unique

 


### -field pCountryOrRegionStringList.size_is

 


### -field pCountryOrRegionStringList.size_is.dwNumberOfItems

 


### -field pCountryOrRegionStringList

A list of supported country or region strings. In Windows, a <b>DOT11_COUNTRY_OR_REGION_STRING</b> is of type <b>char[3]</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>
 

 

