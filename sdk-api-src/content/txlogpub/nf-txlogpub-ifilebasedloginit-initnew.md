---
UID: NF:txlogpub.IFileBasedLogInit.InitNew
title: IFileBasedLogInit::InitNew
author: windows-driver-content
description: Create a new log instance on the specified file. If a file with that name already exists, it is overwritten.
old-location: com\ifilebasedloginit_initnew.htm
old-project: com
ms.assetid: 729c0cfc-4246-4185-af06-ed90a1955b03
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFileBasedLogInit interface [COM],InitNew method, IFileBasedLogInit.InitNew, IFileBasedLogInit::InitNew, InitNew, InitNew method [COM], InitNew method [COM],IFileBasedLogInit interface, _com_ifilebasedloginit_initnew, com.ifilebasedloginit_initnew, txlogpub/IFileBasedLogInit::InitNew
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RECORD_READING_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Txlogpub.h
api_name:
-	IFileBasedLogInit.InitNew
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IFileBasedLogInit::InitNew


## -description


Create a new log instance on the specified file. If a file with that name already exists, it is overwritten.


## -parameters




### -param filename [in]

The absolute path of the file to be created.


### -param cbCapacityHint [in]

A hint to the implementation about the total capacity that will be needed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c499f32b-3897-4c61-b9c1-d660648aab76">IFileBasedLogInit</a>
 

 

