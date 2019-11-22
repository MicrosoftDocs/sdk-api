---
UID: NF:drt.DrtDeletePnrpBootstrapResolver
title: DrtDeletePnrpBootstrapResolver function (drt.h)

description: DrtDeletePnrpBootstrapResolver function deletes a bootstrap resolver based on the Peer Name Resolution Protocol (PNRP).
old-location: p2p\drtdeletepnrpbootstrapresolver.htm
tech.root: P2PSdk
ms.assetid: 0ff7bcc6-548b-475a-8a83-1ca50dbe333d

ms.date: 12/05/2018
ms.keywords: DrtDeletePnrpBootstrapResolver, DrtDeletePnrpBootstrapResolver function [Peer Networking], drt/DrtDeletePnrpBootstrapResolver, p2p.drtdeletepnrpbootstrapresolver
ms.topic: function
f1_keywords: 
 - "drt/DrtDeletePnrpBootstrapResolver"
dev_langs:
 - c++
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtDeletePnrpBootstrapResolver
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtDeletePnrpBootstrapResolver function


## -description


The <b>DrtDeletePnrpBootstrapResolver</b> function deletes a  bootstrap resolver based on the <a href="https://docs.microsoft.com/windows/desktop/P2PSdk/pnrp-namespace-provider-api">Peer Name Resolution Protocol</a> (PNRP).


## -parameters




### -param pResolver [in]

Pointer to the created PNRP bootstrap resolver to be deleted.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver">DrtCreatePnrpBootstrapResolver</a>
 

 

