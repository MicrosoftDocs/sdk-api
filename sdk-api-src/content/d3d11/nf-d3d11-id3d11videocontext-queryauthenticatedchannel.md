---
UID: NF:d3d11.ID3D11VideoContext.QueryAuthenticatedChannel
title: ID3D11VideoContext::QueryAuthenticatedChannel (d3d11.h)
author: windows-sdk-content
description: Sends a query to an authenticated channel.
old-location: mf\id3d11videocontext_queryauthenticatedchannel.htm
tech.root: medfound
ms.assetid: 4E059358-E1FD-4EDB-B1D4-982802385232
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],QueryAuthenticatedChannel method, ID3D11VideoContext.QueryAuthenticatedChannel, ID3D11VideoContext::QueryAuthenticatedChannel, QueryAuthenticatedChannel, QueryAuthenticatedChannel method [Media Foundation], QueryAuthenticatedChannel method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::QueryAuthenticatedChannel, mf.id3d11videocontext_queryauthenticatedchannel
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - ID3D11VideoContext.QueryAuthenticatedChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::QueryAuthenticatedChannel


## -description


Sends a query to an authenticated channel.




## -parameters




### -param pChannel [in]

A pointer to the <a href="https://msdn.microsoft.com/B2DE8E06-1571-4D50-9296-8EB4BB74D6BA">ID3D11AuthenticatedChannel</a> interface.


### -param InputSize [in]

The size of the <i>pInput</i> array, in bytes.


### -param pInput [in]

A pointer to a byte array that contains input data for the query. This array always starts with a <a href="https://msdn.microsoft.com/D1FE4B31-A29D-4079-ABAE-8EB7DB0A0B42">D3D11_AUTHENTICATED_QUERY_INPUT</a> structure. The <b>QueryType</b> member of the structure specifies the query and defines the meaning of the rest of the array.


### -param OutputSize [in]

The size of the <i>pOutput</i> array, in bytes.


### -param pOutput [out]

A pointer to a byte array that receives the result of the query. This array always starts with a <a href="https://msdn.microsoft.com/D5650992-04D0-4DD2-A858-1E7FB979A9C2">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure. The meaning of the rest of the array depends on the query.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

