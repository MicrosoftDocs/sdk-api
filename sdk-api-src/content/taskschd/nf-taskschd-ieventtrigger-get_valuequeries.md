---
UID: NF:taskschd.IEventTrigger.get_ValueQueries
title: IEventTrigger::get_ValueQueries (taskschd.h)
description: Gets or sets a collection of named XPath queries. Each query in the collection is applied to the last matching event XML returned from the subscription query specified in the Subscription property.
helpviewer_keywords: ["IEventTrigger interface [Task Scheduler]","ValueQueries property","IEventTrigger.ValueQueries","IEventTrigger.get_ValueQueries","IEventTrigger::ValueQueries","IEventTrigger::get_ValueQueries","IEventTrigger::put_ValueQueries","ValueQueries property [Task Scheduler]","ValueQueries property [Task Scheduler]","IEventTrigger interface","get_ValueQueries","taskschd.ieventtrigger_valuequeries","taskschd/IEventTrigger::ValueQueries","taskschd/IEventTrigger::get_ValueQueries","taskschd/IEventTrigger::put_ValueQueries"]
old-location: taskschd\ieventtrigger_valuequeries.htm
tech.root: taskschd
ms.assetid: 0bceb9d5-11f3-40a3-ba05-be896420e1db
ms.date: 12/05/2018
ms.keywords: IEventTrigger interface [Task Scheduler],ValueQueries property, IEventTrigger.ValueQueries, IEventTrigger.get_ValueQueries, IEventTrigger::ValueQueries, IEventTrigger::get_ValueQueries, IEventTrigger::put_ValueQueries, ValueQueries property [Task Scheduler], ValueQueries property [Task Scheduler],IEventTrigger interface, get_ValueQueries, taskschd.ieventtrigger_valuequeries, taskschd/IEventTrigger::ValueQueries, taskschd/IEventTrigger::get_ValueQueries, taskschd/IEventTrigger::put_ValueQueries
f1_keywords:
- taskschd/IEventTrigger.ValueQueries
dev_langs:
- c++
req.header: taskschd.h
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- IEventTrigger.ValueQueries
- IEventTrigger.get_ValueQueries
- IEventTrigger.put_ValueQueries
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventTrigger::get_ValueQueries


## -description


Gets or sets a collection of named XPath queries. Each query in the collection is applied to the last matching event XML returned from the subscription query specified in the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription">Subscription</a> property. 

This property is read/write.


## -parameters


## -remarks



The name of the query can be used as a variable in the following action properties:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody">MessageBody property of IShowMessageAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title">Title property of IShowMessageAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments">Arguments property of IExecAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory">WorkingDirectory property of IExecAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server">Server property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject">Subject property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to">To property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc">Cc property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc">Bcc property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto">ReplyTo property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from">From property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body">Body property of IEmailAction</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data">Data property of IComHandlerAction</a>
</li>
</ul>


The following  code example strings show two name-value pairs that can  be used in a name-value collection.
The values returned by the XPath queries can replace variables in an action property. The values are referenced by name,  with $(user) and $(machine), in the action property. For example, if the $(user) and $(machine) variables are used in the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody">MessageBody property of IShowMessageAction</a>, then the value of the XPath queries will replace the variables in the string.

<pre class="syntax" xml:space="preserve"><code>name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName</code></pre>
For more information about writing a query string for certain events, see <a href="https://msdn.microsoft.com/library/aa385231(VS.85).aspx">Event Selection</a> and <a href="https://msdn.microsoft.com/library/aa385771(VS.85).aspx">Subscribing to Events</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection">ITaskNamedValueCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluepair">ITaskNamedValuePair</a>
 

 

