---
UID: NF:shidfact.CItemIDFactory.GetDataFromIDList(PCUIDLIST_RELATIVE,const T)
title: CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE,const T)
author: windows-driver-content
description: Gets a read only pointer to the client provided structure in the first ItemID in the IDList.
old-location: shell\citemidfactory_getdatafromidlist.htm
old-project: shell
ms.assetid: E3E2233D-F424-4BF9-AAC4-4DC2FB75E214
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetDataFromIDList method, CItemIDFactory.GetDataFromIDList, CItemIDFactory.GetDataFromIDList(PCUIDLIST_RELATIVE,const T), CItemIDFactory::GetDataFromIDList, CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE,const T), GetDataFromIDList, GetDataFromIDList method [Windows Shell], GetDataFromIDList method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getdatafromidlist, shidfact/CItemIDFactory::GetDataFromIDList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shidfact.h
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shidfact.h
api_name:
-	CItemIDFactory.GetDataFromIDList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# CItemIDFactory::GetDataFromIDList(PCUIDLIST_RELATIVE,const T)


## -description


Gets a read only pointer to the client provided structure in the first ItemID in the IDList.


## -parameters




### -param pidl [in]

A PIDL containing the data.


#### - ppData [out]

When this method returns, contains the address of a read only pointer to a client provided structure.


## -returns



If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7">CItemIDFactory</a>
 

 

