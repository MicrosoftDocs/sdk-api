---
UID: NF:ntdsapi.DsListInfoForServerA
title: DsListInfoForServerA function (ntdsapi.h)
author: windows-sdk-content
description: The DsListInfoForServer function lists miscellaneous data for a server.
old-location: ad\dslistinfoforserver.htm
tech.root: ad
ms.assetid: 15dcc7ac-4edb-42fa-8466-033794762046
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DS_LIST_ACCOUNT_OBJECT_FOR_SERVER, DS_LIST_DNS_HOST_NAME_FOR_SERVER, DS_LIST_DSA_OBJECT_FOR_SERVER, DsListInfoForServer, DsListInfoForServer function [Active Directory], DsListInfoForServerA, DsListInfoForServerW, _glines_dslistinfoforserver, ad.dslistinfoforserver, ntdsapi/DsListInfoForServer, ntdsapi/DsListInfoForServerA, ntdsapi/DsListInfoForServerW
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListInfoForServerW (Unicode) and DsListInfoForServerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsListInfoForServer
 - DsListInfoForServerA
 - DsListInfoForServerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsListInfoForServerA function


## -description


The <b>DsListInfoForServer</b> function lists miscellaneous data for a server.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param server [in]

Pointer to a null-terminated string that specifies the server name. This name must be the same as one of the strings returned by the <a href="https://msdn.microsoft.com/1e346532-bbbe-4b3b-a1cb-6a72319cb3e2">DsListServersForDomainInSite</a> or <a href="https://msdn.microsoft.com/46773631-d464-4d9e-83e7-aa502599df71">DsListServersInSite</a> function.


### -param ppInfo [out]

Pointer to a variable that receives a pointer to a 
<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure that contains the server data. The returned structure must be deallocated using 
<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>.

The indexes of the array in the <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure indicate what data are contained by each array element. The following constants may be used to specify the desired index for a particular piece of data.



#### DS_LIST_ACCOUNT_OBJECT_FOR_SERVER

Name of the account object for the domain controller (DC).



#### DS_LIST_DNS_HOST_NAME_FOR_SERVER

DNS host name of the DC.



#### DS_LIST_DSA_OBJECT_FOR_SERVER

GUID of the directory service agent (DSA) for the domain controller (DC).


## -returns



If the function returns server data, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.




## -remarks



Individual name conversion errors are reported in the returned <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>
 

 

