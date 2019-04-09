---
UID: NF:netioapi.InitializeUnicastIpAddressEntry
title: InitializeUnicastIpAddressEntry function (netioapi.h)
author: windows-sdk-content
description: Initializes a MIB_UNICASTIPADDRESS_ROW structure with default values for a unicast IP address entry on the local computer.
old-location: iphlp\initializeunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: 8cbdd972-060a-4e18-9490-450df21936ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeUnicastIpAddressEntry, InitializeUnicastIpAddressEntry function [IP Helper], iphlp.initializeunicastipaddressentry, netioapi/InitializeUnicastIpAddressEntry
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - InitializeUnicastIpAddressEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeUnicastIpAddressEntry function


## -description


The 
<b>InitializeUnicastIpAddressEntry</b> function  initializes a <b>MIB_UNICASTIPADDRESS_ROW</b> structure with default values for a unicast IP address entry on the local computer.  


## -parameters




### -param Row [out]

On entry, a pointer to a 
<a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure entry for a unicast IP address entry. On return, the  <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to by this parameter is initialized with default values for a unicast IP address.


## -returns



This function does not return a value.




## -remarks



The <b>InitializeUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeUnicastIpAddressEntry</b> function must be used to initialize the members of a
    <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure entry with default values for a unicast IP address for later use with the <a href="https://msdn.microsoft.com/8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0">CreateUnicastIpAddressEntry</a> function.  

On input, <b>InitializeUnicastIpAddressEntry</b> must be passed a new <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure to initialize. 

On output, the <b>PrefixOrigin</b> member of the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by <i>Row</i> parameter the will be initialized to <b>IpPrefixOriginUnchanged</b>, the <b>SuffixOrigin</b> member will be initialized to <b>IpSuffixOriginUnchanged</b>, and the  <b>OnLinkPrefixLength</b> member will be initialized to an illegal value. In addition, the <b>PreferredLifetime</b> and <b>ValidLifetime</b> members are set to infinite, the <b>SkipAsSource</b> member is set to <b>FALSE</b>, and other fields are initialized to zero. 

After calling <b>InitializeUnicastIpAddressEntry</b>, an application can then change the
    members in the <a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a> entry it wishes to modify, and then call the <a href="https://msdn.microsoft.com/8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0">CreateUnicastIpAddressEntry</a>  to add the new unicast IP address to the local computer.




## -see-also




<a href="https://msdn.microsoft.com/8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0">CreateUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/a630397a-ef4a-40c2-b2e7-3e85cd9e8029">DeleteUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/d5475c09-05dd-41d7-80ff-63c52d78468c">GetUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/bdafc4a4-5f3c-4dd5-ba9b-4f6045a82652">GetUnicastIpAddressTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/f329bafd-9e83-4754-a9a9-e7e111229c90">MIB_UNICASTIPADDRESS_ROW</a>



<a href="https://msdn.microsoft.com/b064494c-d0d5-4570-b255-4cc95412fd3a">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="https://msdn.microsoft.com/56945aa2-ca1e-44b3-9765-d862978a9dbe">NotifyUnicastIpAddressChange</a>



<a href="https://msdn.microsoft.com/906a3895-2e42-4bed-90a3-7c10487d76cb">SetUnicastIpAddressEntry</a>
 

 

