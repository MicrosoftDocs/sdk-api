---
UID: NS:wininet.INTERNET_PER_CONN_OPTION_LISTW
title: INTERNET_PER_CONN_OPTION_LISTW
author: windows-sdk-content
description: Contains the list of options for a particular Internet connection.
old-location: wininet\internet_per_conn_option_list.htm
old-project: wininet
ms.assetid: 5e3178d5-b266-44bd-846c-f14bad0083c4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPINTERNET_PER_CONN_OPTION_LISTW, INTERNET_PER_CONN_OPTION_LIST, INTERNET_PER_CONN_OPTION_LIST structure [WinINet], INTERNET_PER_CONN_OPTION_LISTA, INTERNET_PER_CONN_OPTION_LISTW, LPINTERNET_PER_CONN_OPTION_LIST, LPINTERNET_PER_CONN_OPTION_LIST structure pointer [WinINet], _inet_internet_per_conn_option_list_structure, wininet.internet_per_conn_option_list, wininet/INTERNET_PER_CONN_OPTION_LIST, wininet/INTERNET_PER_CONN_OPTION_LISTA, wininet/INTERNET_PER_CONN_OPTION_LISTW, wininet/LPINTERNET_PER_CONN_OPTION_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wininet.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INTERNET_PER_CONN_OPTION_LISTW (Unicode) and INTERNET_PER_CONN_OPTION_LISTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: INTERNET_PER_CONN_OPTION_LISTW, *LPINTERNET_PER_CONN_OPTION_LISTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_PER_CONN_OPTION_LIST
 - INTERNET_PER_CONN_OPTION_LISTA
 - INTERNET_PER_CONN_OPTION_LISTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# INTERNET_PER_CONN_OPTION_LISTW structure


## -description


Contains the list of options for a particular Internet connection.


## -struct-fields




### -field dwSize

Size of the 
structure, in bytes.


### -field pszConnection

Pointer to a string that contains the name of the RAS connection or <b>NULL</b>, which indicates the default or LAN connection, to set or query options on. 


### -field dwOptionCount

Number of options to query or set. 


### -field dwOptionError

Options that failed, if an error occurs. 


### -field pOptions

Pointer to an array of 
<a href="https://msdn.microsoft.com/35cfc768-1f1d-4be9-8d56-c56c7440513e">INTERNET_PER_CONN_OPTION</a> structures containing the options to query or set. 


## -remarks



In Microsoft Internet Explorer 5, only the ANSI versions of 
<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a> and 
<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a> will work with the 
<b>INTERNET_PER_CONN_OPTION_LIST</b> structure. The Unicode versions will support using the 
<b>INTERNET_PER_CONN_OPTION_LIST</b> structure in later versions of Internet Explorer.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/35cfc768-1f1d-4be9-8d56-c56c7440513e">INTERNET_PER_CONN_OPTION</a>



<a href="https://msdn.microsoft.com/b0bafd3d-8f54-429e-b423-dae3d61b0030">InternetQueryOption</a>



<a href="https://msdn.microsoft.com/578c7130-7426-4a2e-ae0f-ed8a84449b06">InternetSetOption</a>
 

 

