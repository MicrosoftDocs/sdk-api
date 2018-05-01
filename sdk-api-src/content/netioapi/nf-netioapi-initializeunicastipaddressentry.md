---
UID: NF:netioapi.InitializeUnicastIpAddressEntry
title: InitializeUnicastIpAddressEntry function
author: windows-driver-content
description: Initializes a MIB_UNICASTIPADDRESS_ROW structure with default values for a unicast IP address entry on the local computer.
old-location: iphlp\initializeunicastipaddressentry.htm
old-project: IpHlp
ms.assetid: 8cbdd972-060a-4e18-9490-450df21936ea
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: InitializeUnicastIpAddressEntry, InitializeUnicastIpAddressEntry function [IP Helper], iphlp.initializeunicastipaddressentry, netioapi/InitializeUnicastIpAddressEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	InitializeUnicastIpAddressEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# InitializeUnicastIpAddressEntry function


## -description


The 
<b>InitializeUnicastIpAddressEntry</b> function  initializes a <b>MIB_UNICASTIPADDRESS_ROW</b> structure with default values for a unicast IP address entry on the local computer.  


## -parameters




### -param Row [out]

On entry, a pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structure entry for a unicast IP address entry. On return, the  <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to by this parameter is initialized with default values for a unicast IP address.


## -returns



This function does not return a value.




## -remarks



The <b>InitializeUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeUnicastIpAddressEntry</b> function must be used to initialize the members of a
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structure entry with default values for a unicast IP address for later use with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546227">CreateUnicastIpAddressEntry</a> function.  

On input, <b>InitializeUnicastIpAddressEntry</b> must be passed a new <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structure to initialize. 

On output, the <b>PrefixOrigin</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by <i>Row</i> parameter the will be initialized to <b>IpPrefixOriginUnchanged</b>, the <b>SuffixOrigin</b> member will be initialized to <b>IpSuffixOriginUnchanged</b>, and the  <b>OnLinkPrefixLength</b> member will be initialized to an illegal value. In addition, the <b>PreferredLifetime</b> and <b>ValidLifetime</b> members are set to infinite, the <b>SkipAsSource</b> member is set to <b>FALSE</b>, and other fields are initialized to zero. 

After calling <b>InitializeUnicastIpAddressEntry</b>, an application can then change the
    members in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> entry it wishes to modify, and then call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546227">CreateUnicastIpAddressEntry</a>  to add the new unicast IP address to the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546227">CreateUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546370">DeleteUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552589">GetUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552594">GetUnicastIpAddressTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559322">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568809">NotifyUnicastIpAddressChange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570800">SetUnicastIpAddressEntry</a>
 

 

