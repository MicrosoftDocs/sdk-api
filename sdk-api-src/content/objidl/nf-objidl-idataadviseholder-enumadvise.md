---
UID: NF:objidl.IDataAdviseHolder.EnumAdvise
title: IDataAdviseHolder::EnumAdvise (objidl.h)
author: windows-sdk-content
description: Returns an object that can be used to enumerate the current advisory connections.
old-location: com\idataadviseholder_enumadvise.htm
tech.root: com
ms.assetid: 0863d013-6f55-40ce-92d2-68bb0455a911
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IDataAdviseHolder interface, IDataAdviseHolder interface [COM],EnumAdvise method, IDataAdviseHolder.EnumAdvise, IDataAdviseHolder::EnumAdvise, _ole_idataadviseholder_enumadvise, com.idataadviseholder_enumadvise, objidl/IDataAdviseHolder::EnumAdvise
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IDataAdviseHolder.EnumAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataAdviseHolder::EnumAdvise


## -description


Returns an object that can be used to enumerate the current advisory connections.


## -parameters




### -param ppenumAdvise [out]

A pointer to an <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If the implementation returns <b>NULL</b> in *<i>ppenumAdvise</i>, there are no connections to advise sinks at this time.


## -returns



This method returns S_OK if the enumerator object is successfully instantiated or there are no connections.




## -remarks



This method must supply a pointer to an implementation of the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> interface. Its methods allow you to enumerate the data stored in an array of <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structures. You get a pointer to the OLE implementation of <a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a> through a call to <a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>, and then call <b>IDataAdviseHolder::EnumAdvise</b> to implement <a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">IDataObject::EnumDAdvise</a>.

Adding more advisory connections while the enumerator object is active has an undefined effect on the enumeration that results from this method.




## -see-also




<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/319637fd-d9b5-4da0-ac92-4c52fa9f5231">IDataObject::EnumDAdvise</a>



<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>
 

 

