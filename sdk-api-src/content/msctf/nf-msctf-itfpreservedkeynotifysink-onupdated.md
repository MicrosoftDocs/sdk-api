---
UID: NF:msctf.ITfPreservedKeyNotifySink.OnUpdated
title: ITfPreservedKeyNotifySink::OnUpdated
author: windows-driver-content
description: ITfPreservedKeyNotifySink::OnUpdated method
old-location: tsf\itfpreservedkeynotifysink_onupdated.htm
old-project: TSF
ms.assetid: 50654da7-60ee-4038-a02a-1055445f1e5d
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfPreservedKeyNotifySink interface [Text Services Framework],OnUpdated method, ITfPreservedKeyNotifySink.OnUpdated, ITfPreservedKeyNotifySink::OnUpdated, OnUpdated, OnUpdated method [Text Services Framework], OnUpdated method [Text Services Framework],ITfPreservedKeyNotifySink interface, _tsf_itfpreservedkeynotifysink_onupdated_ref, msctf/ITfPreservedKeyNotifySink::OnUpdated, tsf.itfpreservedkeynotifysink_onupdated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfPreservedKeyNotifySink.OnUpdated
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPreservedKeyNotifySink::OnUpdated


## -description




## -parameters




### -param pprekey [in]

Pointer to a <a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">TF_PRESERVEDKEY</a> structure that contains data about the key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To determine if the key is unpreserved, call <a href="https://msdn.microsoft.com/50deac9c-b659-494b-9cda-d6109fa39363">ITfKeystrokeMgr::IsPreservedKey</a>, passing <i>pprekey</i>. If the key is not found, it is unpreserved. If the key is found, it is either preserved or the description has changed. Unless you keep track of the current key description and compare the previous description with the current description in response to this notification, there is no way to determine if this notification is in response to a key preserved or the description changed.




## -see-also




<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://msdn.microsoft.com/feb83f22-652c-4fec-b35d-a0cc41eab533">
        ITfKeystrokeMgr::SetPreservedKeyDescription
      </a>



<a href="https://msdn.microsoft.com/05975fce-04c3-4316-a9b2-ed015e7aa8fe">
        ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="https://msdn.microsoft.com/0bf786b5-efcd-4c58-835b-47e7adf9be63">ITfPreservedKeyNotifySink</a>



<a href="https://msdn.microsoft.com/95d37e94-3991-49c9-bddf-4183a69d49b9">
        TF_PRESERVEDKEY
      </a>
 

 

