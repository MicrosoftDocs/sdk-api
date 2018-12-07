---
UID: NF:msctf.ITfStatusSink.OnStatusChange
title: ITfStatusSink::OnStatusChange
author: windows-sdk-content
description: ITfStatusSink::OnStatusChange method
old-location: tsf\itfstatussink_onstatuschange.htm
tech.root: TSF
ms.assetid: 6eabf08f-006b-43b4-aea7-1d803b3d09b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfStatusSink interface [Text Services Framework],OnStatusChange method, ITfStatusSink.OnStatusChange, ITfStatusSink::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITfStatusSink interface, _tsf_itfstatussink_onstatuschange_ref, msctf/ITfStatusSink::OnStatusChange, tsf.itfstatussink_onstatuschange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfStatusSink.OnStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfStatusSink::OnStatusChange


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface whose status has changed.


### -param dwFlags [in]

Indicates that one of the dynamic flags changed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method receives a callback when one of the flags of the <b>dwDynamicFlags</b> member of the <b>TF_STATUS</b> structure changes value. To obtain the changed flag(s), use the <a href="https://msdn.microsoft.com/a1f193b0-fcfc-4db6-90e9-61d528b08672">ITfContext::GetStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/a1f193b0-fcfc-4db6-90e9-61d528b08672">ITfContext::GetStatus
      </a>



<a href="https://msdn.microsoft.com/5fc37251-938b-4581-bb54-816749b17001">ITfStatusSink</a>



<a href="https://msdn.microsoft.com/1f00c8e1-435c-45ce-892a-36af68154144">TF_STATUS
      </a>
 

 

