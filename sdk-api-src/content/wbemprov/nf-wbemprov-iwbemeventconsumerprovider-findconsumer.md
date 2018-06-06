---
UID: NF:wbemprov.IWbemEventConsumerProvider.FindConsumer
title: IWbemEventConsumerProvider::FindConsumer
author: windows-sdk-content
description: The FindConsumer function locates and returns sink objects to which WMI can send events.
old-location: wmi\iwbemeventconsumerprovider_findconsumer.htm
old-project: WmiSdk
ms.assetid: 196c839a-5b8f-4ff6-b6cf-3483db275e8b
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: FindConsumer, FindConsumer method [Windows Management Instrumentation], FindConsumer method [Windows Management Instrumentation],IWbemEventConsumerProvider interface, IWbemEventConsumerProvider interface [Windows Management Instrumentation],FindConsumer method, IWbemEventConsumerProvider.FindConsumer, IWbemEventConsumerProvider::FindConsumer, _hmm_iwbemeventconsumerprovider_findconsumer, wbemprov/IWbemEventConsumerProvider::FindConsumer, wmi.iwbemeventconsumerprovider_findconsumer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventConsumerProvider.FindConsumer
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemEventConsumerProvider::FindConsumer


## -description


The 
<b>FindConsumer</b> function locates and returns sink objects to which WMI can send events. WMI passes in a pointer to a logical consumer object, then 
<b>FindConsumer</b> locates the physical consumer associated with the logical consumer. Finally, 
<b>FindConsumer</b> returns to WMI a pointer to the sink belonging to the physical consumer. WMI calls <a href="_com_iunknown_addref">AddRef</a> on the sink and begins to deliver the appropriate events to the sink. WMI releases the sink after a configurable period of time with no deliveries. If necessary, WMI can call 
<b>FindConsumer</b> again to load the sink again.


## -parameters




### -param pLogicalConsumer [in]

Pointer to the logical consumer object to which the event objects are to be delivered.


### -param ppConsumer [out]

Returns an event object sink to Windows Management. Windows Management calls <a href="_com_iunknown_addref">AddRef</a> for this pointer and deliver the events associated with the logical consumer to this sink. Eventually, after a suitable time-out, Windows Management calls <a href="_com_iunknown_release">Release</a> for the pointer.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



Windows Management delivers events in the form of 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> to logical consumers registered within the schema. A consumer provider implements 
<b>FindConsumer</b> to provide an event sink to Windows Management whenever events must be delivered to the logical consumer.

Windows Management recognizes the logical consumer object and has the event objects ready for delivery. To deliver an event object, WMI then calls 
<b>FindConsumer</b>. The consumer provider must create an event sink object (a pointer to 
<a href="https://msdn.microsoft.com/a890aefe-e35e-4635-874d-953194f99a82">IWbemUnboundObjectSink</a>), and return the pointer to Windows Management so that the events can be delivered.

Using this technique, a single event consumer provider can handle delivery of events to many different logical consumers by returning different 
<a href="https://msdn.microsoft.com/a890aefe-e35e-4635-874d-953194f99a82">IWbemUnboundObjectSink</a> pointers for each.

You may implement 
<b>FindConsumer</b> in several ways:

<ul>
<li>
Provide a single sink for all logical consumers.

This approach is the most efficient in terms of space because only one COM object is stored in memory. For example, consider an event consumer provider supplying sinks for logical consumers that log messages to files: The single sink bears the responsibility for examining the data included with each logical consumer and determining how to proceed. Most likely, each event received involves opening a log file, logging the message, and closing the file. While efficient in terms of space, this strategy involves a significant amount of processing time.

</li>
<li>
Provide a different sink for each logical consumer.

This approach optimizes performance by having a dedicated sink ready to receive an event as the event occurs. This strategy is faster than a single sink, but less efficient because of its cost in terms of memory. Because each sink maintains its own log file, the file can always be open and ready to log messages as events occur. The sink can then close the file when WMI releases the sink after a time-out, providing efficient performance both in high-speed and in low-speed delivery scenarios.

</li>
<li>
Divide logical consumers into groups and provide a different sink for each group.

This approach compromises between performance and efficiency. The hybrid approach can involve having a few different log files, possibly with each tied to the type of message to be logged. Multiple COM objects handle multiple open files. An event consumer provider taking this approach reads the log file name during the 
<b>FindConsumer</b> call, opens the file, and returns the sink that logs all messages into this file. The provider closes the file on the last call to the <a href="_com_iunknown_release">Release</a> method. With this approach, the consumer preserves efficiency because it has information on exactly which file to use; the consumer is not required to search for or open a new file. Also, the consumer can save memory by combining sinks that log different messages to the same file.

</li>
</ul>
Regardless of approach, your implementation should depend on the existence of an event consumer provider. WMI releases an event consumer provider after a designated interval has elapsed between calls. Because WMI needs your event consumer provider only to supply pointers to sinks for new logical consumers, WMI can release your event consumer provider after your provider services all logical consumers in question. The sinks, however, must remain to receive all of the events that occur.


#### Examples

The following code example describes an implementation of 
<b>FindConsumer</b>. In the implementation following, assume two sinks exist for receiving events, one for each of the two different registered event filters. To determine which sink 
<b>FindConsumer</b> sends back to WMI, the code examines the incoming logical consumer object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT MyEventConsumerClass::FindConsumer(
   /* [in] */ IWbemClassObject __RPC_FAR *pLogicalConsumer,
   /* [out] */ IWbemUnboundObjectSink __RPC_FAR *__RPC_FAR *ppConsumer
   )
{
   // Examine the logical consumer to see which one it is.
   // ====================================================

   VARIANT v;    
   VariantInit(&amp;v);

   HRESULT hRes = WBEM_E_NOT_FOUND;
   *ppConsumer = 0;

   pLogicalConsumer-&gt;Get(_bstr_t(L"Name"), 0, &amp;v, 0, 0);

   // Decide which of the two logical consumers to send back.
   // =======================================================

   if (_wcsicmp(V_BSTR(&amp;v), L"Consumer1") == 0)
   {

    //send back the Consumer1 sink to WMI
    // For example:
      /*hRes =  m_pConsumer1-&gt;
         QueryInterface(IID_IWbemUnboundObjectSink,
                           (LPVOID*)ppConsumer);*/
   }
   else if (_wcsicmp(V_BSTR(&amp;v), L"Consumer2") == 0)
   {
    //send back the Consumer2 sink to WMI
    // For example:
      /*hRes =  m_pConsumer2-&gt;
          QueryInterface(IID_IWbemUnboundObjectSink,
                            (LPVOID*)ppConsumer);*/
   }

   VariantClear(&amp;v);
   return hRes;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/793bbc22-4a8b-4ab3-8cfe-7d81f42a6b7f">IWbemEventConsumerProvider</a>



<a href="https://msdn.microsoft.com/475dca47-b1e5-4362-ab00-9ab9383e92f9">Receiving Events at All Times</a>



<a href="https://msdn.microsoft.com/380ac556-ba0a-4fae-8b76-0645d99e8583">Receiving Events for the Duration of your Application</a>
 

 

