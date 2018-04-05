---
UID: NE:windot11._DOT11_PHY_TYPE
title: "_DOT11_PHY_TYPE"
author: windows-driver-content
description: Defines an 802.11 PHY and media type.
old-location: nwifi\dot11_phy_type.htm
old-project: NativeWiFi
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_PHY_TYPE, DOT11_PHY_TYPE, DOT11_PHY_TYPE enumeration [NativeWIFI], PDOT11_PHY_TYPE, PDOT11_PHY_TYPE enumeration pointer [NativeWIFI], _DOT11_PHY_TYPE, dot11_phy_type_IHV_end, dot11_phy_type_IHV_start, dot11_phy_type_any, dot11_phy_type_dsss, dot11_phy_type_erp, dot11_phy_type_fhss, dot11_phy_type_hrdsss, dot11_phy_type_ht, dot11_phy_type_irbaseband, dot11_phy_type_ofdm, dot11_phy_type_unknown, dot11_phy_type_vht, nwifi.dot11_phy_type, windot11/DOT11_PHY_TYPE, windot11/PDOT11_PHY_TYPE, windot11/dot11_phy_type_IHV_end, windot11/dot11_phy_type_IHV_start, windot11/dot11_phy_type_any, windot11/dot11_phy_type_dsss, windot11/dot11_phy_type_erp, windot11/dot11_phy_type_fhss, windot11/dot11_phy_type_hrdsss, windot11/dot11_phy_type_ht, windot11/dot11_phy_type_irbaseband, windot11/dot11_phy_type_ofdm, windot11/dot11_phy_type_unknown, windot11/dot11_phy_type_vht"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: windot11.h
req.include-header: 
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
req.typenames: DOT11_PHY_TYPE, *PDOT11_PHY_TYPE, DOT11_PHY_TYPE, *PDOT11_PHY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	windot11.h
api_name:
-	DOT11_PHY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DOT11_PHY_TYPE enumeration


## -description


The <b>DOT11_PHY_TYPE</b> enumeration defines an 802.11 PHY and media type.



## -enum-fields




### -field dot11_phy_type_unknown

Specifies an unknown or uninitialized PHY type. 


### -field dot11_phy_type_any

Specifies any PHY type.


### -field dot11_phy_type_fhss

Specifies a frequency-hopping spread-spectrum (FHSS) PHY. Bluetooth devices can use FHSS or an adaptation of FHSS.


### -field dot11_phy_type_dsss

Specifies a direct sequence spread spectrum (DSSS) PHY type. 


### -field dot11_phy_type_irbaseband

Specifies an infrared (IR) baseband PHY type. 


### -field dot11_phy_type_ofdm

Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.  802.11a devices can use OFDM.


### -field dot11_phy_type_hrdsss

Specifies a high-rate DSSS (HRDSSS) PHY type.


### -field dot11_phy_type_erp

Specifies an extended rate PHY type (ERP). 802.11g devices can use ERP.


### -field dot11_phy_type_ht

Specifies the 802.11n PHY type.


### -field dot11_phy_type_vht

Specifies the 802.11ac PHY type. This is the very high throughput PHY type specified in IEEE 802.11ac.

This value is supported on Windows 8.1, Windows Server 2012 R2, and later.


### -field dot11_phy_type_dmg


### -field dot11_phy_type_IHV_start

Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).


### -field dot11_phy_type_IHV_end

Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).


### -field v1_enum




## -remarks



An IHV can assign a value for its proprietary PHY types from <b>dot11_phy_type_IHV_start</b> through <b>dot11_phy_type_IHV_end</b>. The IHV must assign a unique number from this range for each of its proprietary PHY types.






## -see-also




<a href="https://msdn.microsoft.com/f7d3d106-54a9-4bdf-bccf-216cac938995">WLAN_ASSOCIATION_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/db7a9066-d699-4860-90cd-dc3f4bf42549">WLAN_INTERFACE_CAPABILITY</a>
 

 

