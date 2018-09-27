---
UID: NF:pla.ITraceDataProvider.get_KeywordsAll
title: ITraceDataProvider::get_KeywordsAll
author: windows-sdk-content
description: Retrieves the list of keywords that restricts the category of events that you want the provider to write.
old-location: pla\itracedataprovider_keywordsall.htm
tech.root: PLA
ms.assetid: 9ff48234-927b-4b87-a9b8-2a1047b5e3de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITraceDataProvider interface [PLA],KeywordsAll property, ITraceDataProvider.KeywordsAll, ITraceDataProvider.get_KeywordsAll, ITraceDataProvider::KeywordsAll, ITraceDataProvider::get_KeywordsAll, KeywordsAll property [PLA], KeywordsAll property [PLA],ITraceDataProvider interface, get_KeywordsAll, pla.itracedataprovider_keywordsall, pla/ITraceDataProvider::KeywordsAll, pla/ITraceDataProvider::get_KeywordsAll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
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
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataProvider.KeywordsAll
 - ITraceDataProvider.get_KeywordsAll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataProvider::get_KeywordsAll


## -description


Retrieves the list of keywords that restricts the category of events that you want the provider to write. The restrictions are in addition to those provided by the <a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">ITraceDataProvider::KeywordsAny</a> property.

This property is read-only.


## -parameters


## -remarks



The provider writes an event if any of the event's keyword bits match any of the bits set in the <a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">KeywordsAny</a> property. 
The keywords specified in the  <b>KeywordsAll</b> property further restrict the category of events that you want the provider to write. If the event's keyword meets the <b>KeywordsAny</b> condition, the provider will write the event only if all of the bits in the <b>KeywordsAll</b> mask exist in the event's keyword. The <b>KeywordsAll</b> mask is not used if <b>KeywordsAny</b> is zero.

For more information about how the <b>KeywordsAll</b> and <a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">KeywordsAny</a> conditions relate, see the Remarks section of <a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">KeywordsAny</a>.

You use the <a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a> interface to retrieve or set the keywords value. You can use the <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property to retrieve the keywords value (the value of all of the items in the map when combined with the <b>OR</b> operator), or you can enumerate each item in the map to retrieve the individual keyword values.

Likewise, when you set the keywords value, you call the <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> property to set the keywords value, or you can call the <a href="https://msdn.microsoft.com/4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a">IValueMap::Add</a> method to add each individual keyword value.

If you use <a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a> to set the keywords and the value map contains one or more items, PLA searches the collection for matching values and enables them and disables the others. If the value does not exist in the list, PLA adds the keyword (the item is not named).

The <a href="https://msdn.microsoft.com/965a5ac4-a811-4fd3-8862-51d82d27c0e9">IValueMapItem::Key</a> property contains the string representation of the keyword. The <a href="https://msdn.microsoft.com/3f7549aa-2ad6-40f4-ae09-c5130a9c3451">IValueMapItem::Value</a> property contains the keyword value. The <a href="https://msdn.microsoft.com/f23e02bf-217a-44a2-9e1f-e92a39c1b065">IValueMapItem::Enabled</a> property indicates if the keyword is enabled.  You need to use <a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a> interface only when you want to name the keyword or you want to enable or disable keywords without having to add or remove them.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>



<a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">ITraceDataProvider::KeywordsAny</a>
 

 

