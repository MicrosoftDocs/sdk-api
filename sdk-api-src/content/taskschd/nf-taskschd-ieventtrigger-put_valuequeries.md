---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IEventTrigger::put_ValueQueries


## -description


Gets or sets a collection of named XPath queries. Each query in the collection is applied to the last matching event XML returned from the subscription query specified in the <a href="https://msdn.microsoft.com/884b98cd-f782-44af-9534-067198a7f48d">Subscription</a> property. 

This property is read/write.


## -parameters


## -remarks



The name of the query can be used as a variable in the following action properties:<ul>
<li>
<a href="https://msdn.microsoft.com/7a9e4140-a010-4922-83d2-a063322640c6">MessageBody property of IShowMessageAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6ec51ebb-5aa3-4338-bc88-dd8df34d59ac">Title property of IShowMessageAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/623b3ffb-ff0f-46bf-ae3d-146e38c8bbc8">Arguments property of IExecAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7cebc827-2587-46e4-a963-ad0fccfbcec7">WorkingDirectory property of IExecAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c781f189-f27b-4f37-af53-144e1ae8cb75">Server property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e5e6e84-7d2f-4aa3-946f-fe7fac6e49db">Subject property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5144875a-6854-4907-89cd-6438f6adcc49">To property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/23493ac7-0906-4ea3-9445-3dd56c30bb13">Cc property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7f0a4da7-d2de-433a-ab0d-79b9741aae59">Bcc property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/315ec0f3-3a1b-4b83-a934-af1f5d30910a">ReplyTo property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0e85063-73eb-425a-a306-63ac65ab7ec8">From property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c2bc5924-8014-4463-9537-a115266776ee">Body property of IEmailAction</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ce35108-91ed-4df8-8eb3-5a9ebf781567">Data property of IComHandlerAction</a>
</li>
</ul>


The following  code example strings show two name-value pairs that can  be used in a name-value collection.
The values returned by the XPath queries can replace variables in an action property. The values are referenced by name,  with $(user) and $(machine), in the action property. For example, if the $(user) and $(machine) variables are used in the <a href="https://msdn.microsoft.com/7a9e4140-a010-4922-83d2-a063322640c6">MessageBody property of IShowMessageAction</a>, then the value of the XPath queries will replace the variables in the string.

<pre class="syntax" xml:space="preserve"><code>name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName</code></pre>
For more information about writing a query string for certain events, see <a href="http://go.microsoft.com/fwlink/p/?linkid=168218">Event Selection</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=168415">Subscribing to Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>



<a href="https://msdn.microsoft.com/440dc70b-02de-4974-ad2a-462491d12775">ITaskNamedValueCollection</a>



<a href="https://msdn.microsoft.com/b9d186a3-017d-409e-9d67-e74dc69a486a">ITaskNamedValuePair</a>
 

 

