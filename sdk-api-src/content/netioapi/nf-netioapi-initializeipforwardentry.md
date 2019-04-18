---
UID: NF:netioapi.InitializeIpForwardEntry
title: InitializeIpForwardEntry function (netioapi.h)
author: windows-sdk-content
description: Initializes a MIB_IPFORWARD_ROW2 structure with default values for an IP route entry on the local computer.
old-location: iphlp\initializeipforwardentry.htm
tech.root: IpHlp
ms.assetid: 1968c4e5-4b28-4387-a918-3326bc80bb3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeIpForwardEntry, InitializeIpForwardEntry function [IP Helper], iphlp.initializeipforwardentry, netioapi/InitializeIpForwardEntry
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
 - InitializeIpForwardEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitializeIpForwardEntry function


## -description


The 
<b>InitializeIpForwardEntry</b> function  initializes a  <b>MIB_IPFORWARD_ROW2</b> structure with default values for an IP route entry on the local computer.  


## -parameters




### -param Row [out]

On entry, a pointer to a 
<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. On return, the  <b>MIB_IPFORWARD_ROW2</b> structure pointed to by this parameter is initialized with default values for an IP route entry.


## -returns



This function does not return a value.




## -remarks



The <b>InitializeIpForwardEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeIpForwardEntry</b> function must be used to initialize the members of a
    <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry with default values for an IP route entry for later use with the <a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a> function.  

On input, <b>InitializeIpForwardEntry</b> must be passed a new <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure to initialize. 

On output, the <b>ValidLifetime</b> and <b>PreferredLifetime</b> members of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Row</i> parameter will be initialized to infinite and the <b>Loopback</b>,  <b>AutoconfigureAddress</b>, <b>Publish</b>, and <b>Immortal</b> members  will be initialized to <b>TRUE</b>. In addition, the <b>SitePrefixLength</b>,   <b>Metric</b>, and  <b>Protocol</b> members are set to an illegal value and other fields are initialized to zero. 

After calling <b>InitializeIpForwardEntry</b>, an application can then change the
    members in the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> entry it wishes to modify, and then call the <a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>  to add the new IP route entry to the local computer.




## -see-also




<a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/53d5009a-d205-40ce-88e5-fe37e72b5a50">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>
 

 

